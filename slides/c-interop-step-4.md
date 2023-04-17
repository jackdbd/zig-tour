---
layout: default
---
<h1>Step 4 (opt.): create a <span class="color:accent">Zig wrapper</span></h1>

<Transform scale="0.75">

**But why?**

- namespaces
- easier and safer to use (e.g. less risk of buffer overflow)
- better error handling
- extend it with higher level abstractions (e.g. slices instead of pointers)

**How do do it?**

- <Anchor href="https://www.nmichaels.org/zig/wrap-sodium.html" text="Wrapping a C Library with Zig" />
- <Anchor href="https://tiehu.is/blog/zig1" text="Iterative Replacement of C with Zig" />
- <Anchor href="https://rischmann.fr/blog/how-i-built-zig-sqlite" text="How I built zig-sqlite" />

**Examples:**

- <Anchor href="https://github.com/michal-z/zig-gamedev/tree/main/libs/zgui" text="zgui" />
- <Anchor href="https://github.com/michal-z/zig-gamedev/tree/main/libs/zstbi" text="zstbi" />
- <Anchor href="https://github.com/vrischmann/zig-sqlite" text="zig-sqlite" />

</Transform>

<!--
Notes
-->
