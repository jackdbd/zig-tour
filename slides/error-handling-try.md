---
layout: default
---
# Error handling try

<Citation
  author="Andrew Kelley"
  citeHref="https://youtu.be/Gv2I7qTux7g?t=1337"
  citeText="The Road to Zig 1.0 (22:20)">
  <template v-slot:quote>
    <p slot="quote">In order to have high quality software, correct error handling has to be the <span class="color:accent">easiest, most straightforward path</span> for people to follow.</p>
  </template>
</Citation>

In 2 steps:

1. Whenever something might fail, you <code class="inline-code">try</code> it.
1. To handle the failure, you <code class="inline-code">catch</code> it.

Vedi nota **error handling in zig** e **Error, panic or unreachable? - Loris Cro**.

<Anchor 
  href="https://youtu.be/TOIYyTacInM" 
  text="Error, panic or unreachable? - Loris Cro" 
  alt="Loris Cro explains error handling in Zig" />

error traces (!= stack traces) piu' o meno verso 24:00
https://youtu.be/Gv2I7qTux7g?t=1497

Cosa cambia da una applicazione e una libreria? Lo user.
Ecco perche' exceptions + un global catch all vanno bene in una web app.

<!--
Andrew shows that in C the easiest path is to not deal with errors at all. And this is obviously not good.
-->
