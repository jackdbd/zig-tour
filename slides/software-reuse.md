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
Perche’ e’ importante che una ABI sia stabile?
In mancanza di una ABI stabile, **tutte** le parti di un programma dovrebbero essere compilate con la **stessa versione** dello **stesso compiler** per avere la certezza che il programma compilato su un computer A sia equivalente al programma compilato sul computer B.

Dato che questa cosa e’ impossibile, avere una ABI stabile delle varie librerie usate da quel programma, del compiler usato per compilare quel programma, e dei sistemi operativi su cui viene eseguito quel programma, da’ una **ragionevole** certezza che quel programma funzionera’ allo stesso modo sul computer A e sul computer B.

Nota che si tratta di una **ragionevole** certezza, e non di una certezza assoluta, perche’ stabilire una ABI e’ come stabilire una versione per la tua applicazione/libreria. Gli autori possono anche fare del loro meglio per non rompere la compatibilita’ da una versione all’altra, ma non possono avere la certezza matematica di non averla rotto in qualche punto.

Direi che, se progetti una libreria, piu’ low level features usi, piu’ e’ difficile essere sicuri di non aver rotto la compatibilita’ da qualche parte. Ad esempio se il compiler che usi cambia leggermente le ottimizzazioni che fa sul tuo codice e le tue data structures, ho paura che ci sia il rischio di rompere la ABI anche se ci sei stato attento.
-->
