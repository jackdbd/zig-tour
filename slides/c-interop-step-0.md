---
layout: default
# layout: two-cols
---
# Step 0: no zig

<Transform scale="0.65">

Let's say we have a C program <code class="inline-code">singular.c</code> that uses a popular C library: <Anchor href="https://www.cairographics.org/" text="cairo" />.

```c
#define WIDTH 400
#define HEIGHT 400
#include <cairo/cairo.h>
#include <math.h>
#include <stdio.h>

static void get_singular_values (const cairo_matrix_t *matrix, double *major, double *minor)
{...}

static void get_pen_axes (cairo_t *cr, double *major, double *minor)
{...}

static void draw (cairo_t *cr, int width, int height)
{...}

int main (int argc, char *argv[])
{
    int width = WIDTH;
    int height = HEIGHT;
    cairo_surface_t *surface = cairo_image_surface_create (CAIRO_FORMAT_ARGB32, width, height);
    cairo_t *cr = cairo_create (surface);
    draw (cr, width, height);
    cairo_status_t status = cairo_surface_write_to_png (surface, "singular.png");
    printf("cairo surface status = %d (%s)\n", status, cairo_status_to_string (status) );
    return 0;
}
```

We are compiling <code class="inline-code">singular.c</code> using gcc:

```sh
gcc singular.c -Wall -lm -lcairo -o singular
```

</Transform>

<!--
In gcc:
-lm: links the math library
-lcairo: links the cairo library
-->
