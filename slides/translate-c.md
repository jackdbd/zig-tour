---
layout: two-cols
---
# zig translate-c 1/2

<Transform scale="0.75">

<div>
  <p>
  Let's say we have this <code class="inline-code">cairo_hello.c</code> file:
  </p>
</div>


```c
#include <cairo/cairo.h>

int main (int argc, char *argv[])
{
    cairo_surface_t *surface = 
      cairo_image_surface_create (
        CAIRO_FORMAT_ARGB32, 240, 80
    );
    cairo_t *cr = cairo_create (surface);

    cairo_select_font_face (
        cr,
        "serif",
        CAIRO_FONT_SLANT_NORMAL,
        CAIRO_FONT_WEIGHT_BOLD
    );
    cairo_set_font_size (cr, 32.0);
    cairo_set_source_rgb (cr, 0.0, 0.0, 1.0);
    cairo_move_to (cr, 10.0, 50.0);
    cairo_show_text (cr, "Hello, world");

    cairo_destroy (cr);
    cairo_surface_write_to_png (
        surface, "hello.png"
    );
    cairo_surface_destroy (surface);
    return 0;
}
```

</Transform>

::right::

# zig translate-c 2/2

<Transform scale="0.75">

We can convert it into a Zig file using this command:

```sh
zig translate-c cairo_hello.c \
  -lc -lcairo \
  > cairo_hello.zig
```

Then we can try compiling it with this command:

```sh
zig build-exe cairo_hello.zig \
  -lc -lcairo \
  -O ReleaseSmall
```

The translation might not be complete, so check:

```sh
cat cairo_hello.zig  | grep 'unable to translate'
```

You can use <code class="inline-code">zig translate-c</code> to:

- <Anchor href="https://zig.news/sobeston/using-zig-and-translate-c-to-understand-weird-c-code-4f8" text="understand weird C code" />
- learn about the symbols exported by a C library
- produce Zig code before editing it into more idiomatic code (when you want to create a Zig wrapper for a C library)

</Transform>