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

**How to do it?**

- <Anchor href="https://www.nmichaels.org/zig/wrap-sodium.html" text="Wrapping a C Library with Zig" />
- <Anchor href="https://tiehu.is/blog/zig1" text="Iterative Replacement of C with Zig" />
- <Anchor href="https://rischmann.fr/blog/how-i-built-zig-sqlite" text="How I built zig-sqlite" />

**Examples:**

- <Anchor href="https://github.com/guidorice/libgeos.zig" text="libgeos.zig" />
- <Anchor href="https://github.com/michal-z/zig-gamedev/tree/main/libs/zgui" text="zgui" />
- <Anchor href="https://github.com/jackdbd/zig-cairo" text="zig-cairo" />
- <Anchor href="https://github.com/vrischmann/zig-sqlite" text="zig-sqlite" />
- <Anchor href="https://github.com/fubark/zig-v8" text="zig-v8" />
- <Anchor href="https://github.com/michal-z/zig-gamedev/tree/main/libs/zstbi" text="zstbi" />

</Transform>

<!--
I need to update zig-cairo when the package manager is ready. But also I need to understand whether it makes sense to use cairo when there is skia.
-->
