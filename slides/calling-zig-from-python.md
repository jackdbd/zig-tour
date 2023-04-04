---
layout: default
---
# Calling Zig from Python

<Transform scale="1">

- Zig **dynamic** library <Anchor href="https://ziglang.org/documentation/master/#Exporting-a-C-Library" text="exported to C" /> as <Anchor href="https://docs.python.org/3.10/extending/extending.html?highlight=extension#extending-python-with-c-or-c" text="Python extension module" /> (CPython only)

- <Anchor href="https://docs.python.org/3/library/ctypes.html" text="ctypes" />

- <Anchor href="https://cffi.readthedocs.io/en/latest/" text="cffi" />

Example: <Anchor 
  href="https://zig.news/pyrolistical/how-to-escape-python-and-write-more-zig-228m" 
  text="How to escape Python and write more Zig" 
  alt="How to escape Python and write more Zig on zig.news" />

- Python <Anchor href="https://docs.python.org/3.11/c-api/stable.html#stable-application-binary-interface" text="Limited API" /> (recommended approach? 🤔)

ABI stable across versions, backward/forward compatibility.

```text
const py = @cImport({
    @cDefine("PY_SSIZE_T_CLEAN", {});
    @cInclude("Python.h");
});
```

Watch: <Anchor 
  href="https://youtu.be/AKhqFOdjUfg?t=263" 
  text="Using Zig to write native extension modules for Python - Adam Serafini" />

</Transform>

<!-- 
When a zig functon is to be consumed by a C ABI, prepend it with `export` instead of `pub`.

I think your Zig library must be compiled as a dynamic library. I don't think ctypes and cffi would work with a static library.

Python provides a Stable ABI: a set of symbols that will remain compatible across Python 3.x versions. The Stable ABI contains symbols exposed in the Limited API, but also other ones – for example, functions necessary to support older versions of the Limited API.
-->
