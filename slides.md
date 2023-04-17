---
# https://sli.dev/custom/#frontmatter-configures
# Try CSS classes here:
# https://unocss.dev/interactive/
# class: 'text-center'
css: unocss
defaults:
  layout: center
download: 'https://raw.githubusercontent.com/jackdbd/zig-tour/main/assets/zig-tour.pdf'
# persist drawings in exports and build
drawings:
  persist: false
# Exporting to PDF or PNG requires Playwright for rendering.
# You will therefore need to install playwright-chromium
# https://sli.dev/guide/exporting.html
exportFilename: 'zig-tour'
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
# https://sli.dev/guide/presenter-mode.html
presenter: true
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
src: ./slides/while-1.md
---

---
src: ./slides/while-2.md
---

---
src: ./slides/for-1.md
---

---
src: ./slides/for-2.md
---

---
src: ./slides/comptime-defined-types.md
---

---
src: ./slides/dynamic-vs-static.md
---

---
src: ./slides/software-reuse.md
---

---
src: ./slides/c-interop-intro.md
---

---
src: ./slides/c-interop-step-0.md
---

---
src: ./slides/c-interop-step-1.md
---

---
src: ./slides/c-interop-step-2.md
---

---
src: ./slides/c-interop-step-3-a.md
---

---
src: ./slides/c-interop-step-3-b.md
---

---
src: ./slides/c-interop-step-3-c.md
---

---
src: ./slides/c-interop-step-3-d.md
---

---
src: ./slides/c-interop-step-4.md
---

---
src: ./slides/translate-c.md
---

---
src: ./slides/calling-zig-from-higher-level-languages.md
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
src: ./slides/compilation-targets.md
---

---
src: ./slides/build-modes.md
---

---
src: ./slides/cool-projects.md
---

---
src: ./slides/meme-cat.md
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
src: ./slides/how-do-i-learn-zig.md
---

---
src: ./slides/outro.md
---
