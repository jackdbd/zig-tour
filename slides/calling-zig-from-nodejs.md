---
layout: default
---
# Calling Zig from Node.js

- Zig **dynamic** library that calls V8, libuv, Node.js built-ins, exported as <Anchor href="https://nodejs.org/api/addons.html" text="C++ addon" />

- <Anchor href="https://github.com/nodejs/nan" text ="Native Abstractions for Node.js (nan)" />

- <Anchor href="https://nodejs.org/api/n-api.html" text="Node-API (formerly known as N-API)" /> (recommended approach 🥇)

ABI stable across versions, backward/forward compatibility.

- <Anchor href="https://nodejs.org/api/wasi.html" text="lib/wasi.js" /> (Node.js WebAssembly System Interface, WASI)

<!--
🥇 👍
There are three options for implementing addons: Node-API, nan, or direct use of internal V8, libuv, and Node.js libraries. Unless there is a need for direct access to functionality which is not exposed by Node-API, use Node-API. Refer to C/C++ addons with Node-API for more information on Node-API.

Although Node-API provides an ABI stability guarantee, other parts of Node.js do not, and any external libraries used from the addon may not.

Node-API is backward and forward compatible.

A native addon author can take advantage of the N-API forward compatibility guarantee by ensuring that the addon makes use only of APIs defined in node_api.h and data structures and constants defined in node_api_types.h.
-->
