---
layout: default
---
<h1>Step 2: use the <span class="color:accent">Zig toolchain</span> to build</h1>

<Transform scale="0.75">

<p>
Use <code class="inline-code">build.zig</code> to compile <code class="inline-code">singular.c</code>. Now we an compile our project by typing <code class="inline-code">zig build</code>.
</p>

```text {all|5-17|19-22|24-26|all}
const std = @import("std");
const Build = std.build;

pub fn build(b: *Build) void {
    const target = b.standardTargetOptions(.{});
    const optimize = b.standardOptimizeOption(.{});

    const exe = b.addExecutable(.{
        .name = "singular",
        .root_source_file = .{ .path = "singular.c" },
        .optimize = optimize,
        .target = target,
    });

    exe.linkSystemLibrary("c");
    exe.linkSystemLibrary("cairo");
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
There is still no zig code at this point. We are just using the zig toolchain to build our C project.

Now we can:

- getting rid of any other build dependency (shell scripts, make, cmake, ninja, etc.)
- compile: `zig build install` (you can omit `install` because it's the default task)
- compile and run: `zig build run`
- install project dependencies (i.e. cairo): `zig build install-cairo`
- check which tasks we can do: `zig build -h`

The quickest way to familiarize yourself with the build.zig documentation is:

1. mkdir foo && cd foo
2. zig init-exe
3. Have a look at the generated build.zig

See also:

- https://mitchellh.com/zig/build-internals
-->
