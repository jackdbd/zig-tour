---
layout: default
---
# Build modes (optimizations)

| Mode | Compilation speed | Safety checks | Runtime performance | Binary size | Reproducible build |
| --- | --- | --- | --- | --- | --- |
| <code class="inline-code">Debug</code> (default) | **fast** | ✅ | slow | large | ❌ |
| <code class="inline-code">ReleaseFast</code> | slow | ❌ | **fast** | large | ✅ |
| <code class="inline-code">ReleaseSafe</code> | slow | ✅ | medium | large | ✅ |
| <code class="inline-code">ReleaseSmall</code> | slow | ❌ | medium | **small** | ✅ |

You can also use <code class="inline-code">@setRuntimeSafety(false)</code> to <Anchor href="https://ziglang.org/documentation/master/#setRuntimeSafety" text="disable runtime safety checks" /> for individual scopes.

<!--
Notes
-->
