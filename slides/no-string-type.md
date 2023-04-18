---
layout: two-cols
---
# No string type

<Transform scale="0.85">

<p>How long is the string <span class="color:accent">日本</span> ?</p>

<v-click>

<Citation
  author="Joel Spolsky"
  citeHref="https://www.joelonsoftware.com/2003/10/08/the-absolute-minimum-every-software-developer-absolutely-positively-must-know-about-unicode-and-character-sets-no-excuses/"
  citeText="The Absolute Minimum Every Software Developer Absolutely, Positively Must Know About Unicode and Character Sets (No Excuses!)">
  <template v-slot:quote>
    <p slot="quote">
    It does not make sense to have a string without knowing what <span class="color:accent">encoding</span> it uses.
    </p>
  </template>
</Citation>

See <Anchor 
  href="https://ziglang.org/documentation/master/#String-Literals-and-Unicode-Code-Point-Literals" 
  text="String Literals and Unicode Code Point Literals" 
  alt="String Literals and Unicode Code Point Literals in the Zig documentation" /> in the documentation.

</v-click>

</Transform>

::right::

<v-click>

# What about Zig?

<Transform scale="0.85">
<p>The encoding of a string in Zig is de-facto assumed to be UTF-8.</p>

<p>So <span class="color:accent">日本</span> is 2 code points long, and 6 <code class="inline-code">u8</code> long.</p>
</Transform>

</v-click>


<!--
https://www.huy.rocks/everyday/01-04-2022-zig-strings-in-5-minutes

https://github.com/JakubSzark/zig-string

https://stackoverflow.com/questions/66527365/how-to-concat-two-string-literals-at-compile-time-in-zig

Kanji is U+4e00 to U+9faf, UTF8 3 bytes are U+0800 to U+FFFF.
https://stackoverflow.com/questions/3678752/are-all-kanji-characters-in-utf-8-3-bytes-long

The first 128 code points (ASCII) need one byte.

The next 1,920 code points need two bytes to encode, which covers the remainder of almost all Latin-script alphabets, and also IPA extensions, Greek, Cyrillic, Coptic, Armenian, Hebrew, Arabic, Syriac, Thaana and N'Ko alphabets, as well as Combining Diacritical Marks.

Three bytes are needed for the remaining 61,440 code points of the Basic Multilingual Plane (BMP), which are virtually all the rest in common use,[19] including most Chinese, Japanese and Korean characters.

Four bytes are needed for the 1,048,576 code points in the other planes of Unicode, which include less common CJK characters, various historic scripts, mathematical symbols, and emoji (pictographic symbols).
-->
