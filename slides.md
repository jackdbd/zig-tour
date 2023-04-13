---
# https://sli.dev/custom/#frontmatter-configures
# https://sli.dev/custom/directory-structure.html
# Try CSS here:
# https://unocss.dev/interactive/
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
# background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
# class: 'text-center'
css: unocss
defaults:
  layout: center
# enable pdf downloading in SPA build, can also be a custom url
download: false
# persist drawings in exports and build
drawings:
  persist: false
# Exporting to PDF or PNG requires Playwright for rendering.
# You will therefore need to install playwright-chromium
# https://sli.dev/guide/exporting.html
# exportFilename: 'zig-tour'
highlighter: shiki
htmlAttrs:
  dir: 'ltr'
  lang: 'en'
info: |
  ## Zig tour

  Presentation on Zig I gave at [pisa.dev](https://pisa.dev/).

  Learn more about Zig at [ziglang.org](https://ziglang.org/).
# show line numbers in code blocks
lineNumbers: true
src: ./slides/intro.md
theme: default
# theme: seriph
transition: slide-left
---

---
src: ./slides/speaker.md
---

---
src: ./slides/why-zig.md
---

---
src: ./slides/why-not-other-languages.md
---

---
src: ./slides/meme-vince.md
---

---
src: ./slides/learn-zig-to-learn-how-computers-work.md
---

---
src: ./slides/zen.md
---

---
src: ./slides/keywords.md
---

---
src: ./slides/what-zig-leaves-out.md
---

---
src: ./slides/operator-overloading.md
---

---
src: ./slides/error-handling-intro.md
---

---
src: ./slides/error-definition-js-vs-zig.md
---

---
src: ./slides/error-handling-js-vs-zig.md
---

---
src: ./slides/error-handling-try-catch-panic.md
---

---
src: ./slides/error-handling-tips.md
---

---
src: ./slides/dynamic-vs-static.md
---

---
src: ./slides/software-reuse.md
---

---
src: ./slides/calling-zig-from-python.md
---

---
src: ./slides/calling-zig-from-nodejs.md
---

---
src: ./slides/calling-zig-from-jvm-languages.md
---

---
src: ./slides/webassembly.md
---

---
src: ./slides/webassembly-demo.md
---

---
src: ./slides/strings.md
---

---
src: ./slides/string-concatenation.md
---

---
src: ./slides/arrays-vs-slices.md
---

---
src: ./slides/build-modes.md
---

---
src: ./slides/compilation-targets.md
---

---
src: ./slides/zigup.md
---

---
src: ./slides/setup-vscode.md
---

---
src: ./slides/using-libraries.md
---

---
src: ./slides/cool-projects.md
---

---
src: ./slides/memory-allocation.md
---

---
src: ./slides/memory-allocator-interface.md
---

---
src: ./slides/memory-allocators.md
---

---
src: ./slides/comptime.md
---

---
src: ./slides/reflection.md
---

---
src: ./slides/learning-material.md
---

---
src: ./slides/outro.md
---

---
src: ./slides/meme-cat.md
---
