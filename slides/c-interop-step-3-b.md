---
layout: default
---
<h1>Step 3: replace <span class="color:accent">some</span> C with Zig: <code class="inline-code">singular.zig</code></h1>

<Transform scale="0.75">

<p>
We create a <code class="inline-code">singular.zig</code> where we define the program.
</p>

```text {all}
const std = @import("std");
const c = @import("c.zig");

// The draw function is defined in singular.c, not here in singular.zig
extern "c" fn draw(cr: *c.struct__cairo, width: usize, height: usize) void;

pub fn main() !void {
    const width = 400;
    const height = 400;
    var surface = c.cairo_image_surface_create(c.CAIRO_FORMAT_ARGB32, width, height);
    var cr = c.cairo_create(surface);
    draw(cr.?, width, height);
    var status = c.cairo_surface_write_to_png(surface, "singular.png");
    std.debug.print("status {any}\n", .{status});
}
```

<code class="inline-code">extern</code> can be used to declare a function or variable that will be resolved:

- at link time, when linking statically
- at runtime, when linking dynamically

</Transform>

<!--
The extern keyword or @extern builtin function can be used to link against a variable that is exported from another object. 
-->
