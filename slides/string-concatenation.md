---
layout: default
---
<h1>Speaking of strings...</h1>

<Transform scale="0.85">

This is valid Zig code, if...

```
const s = "foo " ++ way_too_many_characters ++ " bar";
```

<v-click>

If <code class="inline-code">way_too_many_characters</code> is <span class="color:accent">compile-time</span> known.

If <code class="inline-code">way_too_many_characters</code> is <span class="color:accent">runtime</span> known, we <code class="inline-code">try</code> to allocate (and handle allocation failure).

```text {all|12-13}
const std = @import("std");

pub fn main() !void {
    var gpa = std.heap.GeneralPurposeAllocator(.{}){};
    defer std.debug.assert(!gpa.deinit());

    const allocator = gpa.allocator();

    // Let's say way_too_many_characters depends on the content of a file,
    // or from the user's input. So it's runtime known.

    const s = try std.fmt.allocPrint(allocator, "foo {s} bar", .{ way_too_many_characters });
    defer allocator.free(s);

    const stdout = std.io.getStdOut().writer();
    try stdout.print("{s}\n", .{ s });
}
```

</v-click>

</Transform>

<!--
Comptime also introduces the operators ++ and ** for concatenating and repeating arrays and slices. These operators do not work at runtime. Are they syntactic sugar on top of comptime?

var file = try std.fs.cwd().openFile("foo.txt", .{});
defer file.close();
var buf_reader = io.bufferedReader(file.reader());
var in_stream = buf_reader.reader();
var buf: [1024]u8 = undefined;
while (try in_stream.readUntilDelimiterOrEof(&buf, '\n')) |line| {
    // do something with line...
}
-->
