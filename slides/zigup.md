---
layout: default
---
# How to get zig?

<div>
  <p>Download and manage zig compilers with <Anchor href="https://github.com/marler8997/zigup" text="zigup" alt="zigup repo on GitHub" />
  </p>
</div>

**Installation**

```sh
wget https://github.com/marler8997/zigup/releases/download/v2022_08_25/zigup.ubuntu-latest-x86_64.zip
unzip zigup.ubuntu-latest-x86_64.zip
chmod u+x zigup
mv zigup ~/bin/zigup
```

**Usage**

```sh
zigup fetch master
zigup fetch 0.10.1

zigup list

zigup default 0.11.0-dev.2477+2ee328995
zigup default 0.10.1
```

Double-check with <code class="inline-code">zig version</code>.

<!--
Similar to nvm, volta or asdf
https://asdf-vm.com/
-->
