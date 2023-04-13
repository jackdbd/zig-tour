---
layout: default
---
# Strings

<Quiz 
  :answers="[2, 6, 'We cannot answer this question']">
  <template v-slot:question>
    <span>How long is the string <span class="color:accent">日本</span> ?</span>
  </template>
</Quiz>

<v-click>

<br>

<Citation
  author="Joel Spolsky"
  citeHref="https://www.joelonsoftware.com/2003/10/08/the-absolute-minimum-every-software-developer-absolutely-positively-must-know-about-unicode-and-character-sets-no-excuses/"
  citeText="The Absolute Minimum Every Software Developer Absolutely, Positively Must Know About Unicode and Character Sets (No Excuses!)">
  <template v-slot:quote>
    <p slot="quote">
    It does not make sense to have a string without knowing what encoding it uses.
    </p>
  </template>
</Citation>

See <Anchor 
  href="https://ziglang.org/documentation/master/#String-Literals-and-Unicode-Code-Point-Literals" 
  text="String Literals and Unicode Code Point Literals" 
  alt="String Literals and Unicode Code Point Literals in the Zig documentation" /> in the documentation.

</v-click>