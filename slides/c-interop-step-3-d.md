---
layout: default
---
<h1>Step 3: replace <span class="color:accent">some</span> C with Zig: minor fixes</h1>

<Transform scale="0.75">

If we now try to compile our project with <code class="inline-code">zig build</code>, we get:

```sh
error: ld.lld: duplicate symbol: main
```

That's because we have two <code class="inline-code">main</code> functions: one in <code class="inline-code">singular.zig</code> and one in <code class="inline-code">singular.c</code>.

If we remove the <code class="inline-code">main</code> function in <code class="inline-code">singular.c</code> and try again, we get:

```sh
error: ld.lld: undefined symbol: draw
```

That's because we declared the <code class="inline-code">draw</code> function using <code class="inline-code">static</code>.

We change this:

```c
static void draw (cairo_t *cr, int width, int height)
```

into this:

```c
void draw (cairo_t *cr, int width, int height)
```

Now <code class="inline-code">zig build</code> can successfully compile the project.

💡 Watch <Anchor href="https://youtu.be/ySY_FlA7EvA" text="Understanding the Extern Keyword in C" /> if you need a refresher about <code class="inline-code">static</code> and <code class="inline-code">extern</code>.

</Transform>

<!--
Note: we didn't touch the other C functions:

- get_pen_axes
- get_singular_values
-->
