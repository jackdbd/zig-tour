---
layout: default
---
<h1>Step 3: replace <span class="color:accent">some</span> C with Zig: new <code class="inline-code">build.zig</code></h1>

<Transform scale="0.75">

```text {all|10,17|all}
const std = @import("std");
const Build = std.build;

pub fn build(b: *Build) void {
    const target = b.standardTargetOptions(.{});
    const optimize = b.standardOptimizeOption(.{});

    const exe = b.addExecutable(.{
        .name = "singular",
        .root_source_file = .{.path = "singular.zig"},
        .optimize = optimize,
        .target = target,
    });

    exe.linkSystemLibrary("c");
    exe.linkSystemLibrary("cairo");
    exe.addCSourceFile("cairo-svd.c", &[_][]const u8{});
    exe.install();

    const run_cmd = exe.run();
    run_cmd.step.dependOn(b.getInstallStep());
    const run_step = b.step("run", "Run the app");
    run_step.dependOn(&run_cmd.step);

    const install_cairo = b.addSystemCommand(&.{ "sudo", "apt", "install", "libcairo2-dev" });
    const cairo_step = b.step("install-cairo", "Install cairo");
    cairo_step.dependOn(&install_cairo.step);
}
```

</Transform>

<!--
Notes
-->
