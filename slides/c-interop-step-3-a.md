---
layout: default
---
<h1>Step 3: replace <span class="color:accent">some</span> C with Zig: <code class="inline-code">c.zig</code></h1>

<Transform scale="0.75">

<p>
We create a <code class="inline-code">c.zig</code> file where we import all C libraries.
</p>

```text {all}
pub usingnamespace @cImport({
    // XCB is only required when using the XCB surface backend for Cairo.
    @cInclude("xcb/xcb.h");
    @cInclude("cairo/cairo-pdf.h");
    @cInclude("cairo/cairo-script.h");
    @cInclude("cairo/cairo-svg.h");
    @cInclude("cairo/cairo-xcb.h");
    @cInclude("cairo/cairo.h");
    // Leave pango and pangocairo out for now. They would require
    // additional dependencies and they are not used in our program.
    // @cInclude("pango/pangocairo.h");
});
```

</Transform>

<!--
notes
-->
