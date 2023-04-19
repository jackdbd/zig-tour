# How to solve software reuse?

<div>
  <p>We need a (modern-day) lingua franca. Let's review a few key terms.</p>
</div>

<Citation
  citeHref="https://en.wikipedia.org/wiki/Application_binary_interface"
  citeText="Application Binary Interface on Wikipedia">
  <template v-slot:quote>
    <p slot="quote">
    An ABI defines how data structures or computational routines are accessed in machine code, which is a low-level, hardware-dependent format. [...] A common aspect of an ABI is the calling convention, which determines how data is provided as input to, or read as output from, computational routines.
    </p>
  </template>
</Citation>

<br>

<Citation
  citeHref="https://en.wikipedia.org/wiki/Foreign_function_interface"
  citeText="Foreign Function Interface on Wikipedia">
  <template v-slot:quote>
    <p slot="quote">
    A foreign function interface (FFI) is a mechanism by which a program written in one programming language can call routines or make use of services written or compiled in another one. An FFI is often used in contexts where calls are made into binary dynamic-link library.
    </p>
  </template>
</Citation>

A popular FFI is <Anchor 
  href="https://github.com/libffi/libffi" 
  text="libffi/libffi" 
  alt="libffi repo on GitHub" />, which is used by Python (ctypes, cffi), Ruby, Haskell, etc.

<!--
Without a stable ABI, **all** parts of a program should be compiled with the **same version** of the **same compiler** to be sure that the program compiled on computer A is equivalent to the program compiled on computer B.

With a stable ABI, we can be **reasonably** sure that the program compiled on computer A will run on computer B.
-->
