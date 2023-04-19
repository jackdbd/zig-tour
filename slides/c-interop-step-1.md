---
layout: default
---
<h1>Step 1: replace gcc with <span class="color:accent">zig cc</span></h1>

<Transform scale="0.85">

Replace <code class="inline-code">gcc</code> with <code class="inline-code">zig cc</code>:

```sh
zig cc singular.c -lm -lcairo -o singular
```

See <Anchor href="https://andrewkelley.me/post/zig-cc-powerful-drop-in-replacement-gcc-clang.html" text="zig cc: a Powerful Drop-In Replacement for GCC/Clang" />.

**But why?**

- artifact caching
- cross compilation
- pick the libc you want to use / can use
- sane defaults (e.g. <code class="inline-code">-Wall</code> for warnings, <code class="inline-code">fsanitize=undefined</code> for undefined behavior sanitizer)

</Transform>

<!--
https://ruoyusun.com/2022/02/27/zig-cc.html

https://nathancraddock.com/blog/2022/zig-cc-undefined-behavior/

Use `zig cc --verbose` if you want to see all compiler flags set by default.
-->
