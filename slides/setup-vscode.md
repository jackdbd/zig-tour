# Setup VS Code

Just one line.

Install the VS Code extension <Anchor href="https://marketplace.visualstudio.com/items?itemName=ziglang.vscode-zig" text="ziglang.vscode-zig" /> and declare it in your <code class="inline-code">.vscode/extensions.json</code>

```json
{
    "recommendations": ["ziglang.vscode-zig"]
}
```

<code class="inline-code">ziglang.vscode-zig</code> automatically installs the <Anchor href="https://install.zigtools.org/" text="Zig Language Server (zls)" /> for autocompletion, goto definition, formatting, etc.

If you prefer, you can also download zls from <Anchor 
  href="https://github.com/zigtools/zls" 
  text="zigtools/zls" 
  alt="Zig Language Server (zls) repo on GitHub" /> and compile it yourself.

<!--
Zig Language Server (zls) implements Microsoft's Language Server Protocol for Zig in Zig.
-->
