---
layout: default
---
# Using libraries

<div>
Current status: a bit messy. <Anchor 
  href="https://www.reddit.com/r/Zig/comments/rf6crq/whats_the_proper_way_to_installuse_library/" 
  text="What's the proper way to install/use library?" 
  alt="Discussion in r/Zig on the proper way to install and use a zig library." />
</div>

Current solutions:

- <Anchor href="https://github.com/nektro/zigmod" text="nektro/zigmod" />
- <Anchor href="https://github.com/mattnite/gyro" text="mattnite/gyro" />
- <Anchor href="https://github.com/marler8997/zig-build-repos" text="marler8997/zig-build-repos" />
- git submodules
- just copy the source files in your project

The official package manager is near:

- <Anchor href="https://devlog.hexops.com/2023/zig-0-11-breaking-build-changes/" text="Zig tips: v0.11 std.build API / package manager changes"/>
- <Anchor href="https://github.com/ziglang/zig/issues/14307" text="build system terminology update: package, project, module, dependency (issue #14307)" />

<!--
At the moment is a bit messy but soon it will be better.

Run build.zig logic in a WebAssembly sandbox #14286
https://github.com/ziglang/zig/issues/14286
-->
