# Why not C / C++ / Rust?

<Transform scale="1.0">

<Anchor 
href="https://ziglang.org/learn/why_zig_rust_d_cpp/" 
text="Why Zig When There is Already C++, D, and Rust?" />

**C++**

- Complex, too many features
- Error handling tipically done using exceptions
- Why should I have written ZeroMQ in C, not C++, <Anchor href="https://250bpm.com/blog:4/" text="part 1" /> and <Anchor href="https://250bpm.com/blog:8/" text="part 2" />

**C**

- Footguns everywhere
- Preprocessor macros

**Rust**

- Complex, ownership and lifetimes are hard to understand
- <Anchor href="https://twitter.com/rust_foundation/status/1644132378858729474" text="Questionable policies" />

</Transform>

<!--
The author of ZeroMQ did NOT use C++ exceptions, but in the constructor/destructur you kind of have to use them.

Explain what ZeroMQ is. And why C is a better candidate than C++ for this kind of fault-tolerant software.

Consider what happens when **initialisation** of an object can fail. Constructors have no return values, so failure can be reported only by throwing an exception. However, I've decided not to use exceptions.

Moreover, even if initialisation wasn't a problem, **termination** definitely is. You can't really throw exceptions in the destructor. Not because of some self-imposed artificial restrictions but because if the destructor is invoked in the process or unwinding the stack and it happens to throw an exception, it crashes the entire process.
-->