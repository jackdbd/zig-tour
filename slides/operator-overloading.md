---
layout: two-cols
---
# Operator overloading

What does this Python code print?

<Transform :scale="0.75">

```python
a = Foo(2)
b = Bar(3)

print(a + b)
print(b + a)
```

<v-click>

We need to know what <code class="inline-code">+</code> <span class="color:accent">means</span> for <code class="inline-code">a</code> and <code class="inline-code">b</code>.

```python {5-6,12-13|all}
class Foo(object):
    def __init__(self, n):
        self.n = n

    def __add__(self, other):
        return self.n + other.n

class Bar(object):
    def __init__(self, n):
        self.n = n

    def __add__(self, other):
        return self.n - other.n
```

</v-click>

<v-after>

Solution:

```sh
5
1
```

</v-after>

</Transform>

::right::

<v-click>

# Why not?

Arguments in favor of / against operator overloading.

- <Anchor href="https://github.com/ziglang/zig/issues/427" text="Proposal: Custom Operators / Infix Functions (issue #427)" />
- <Anchor href="https://github.com/ziglang/zig/issues/871" text="Operator Overloading (issue #871)" />
- <Anchor href="https://www.reddit.com/r/Zig/comments/fbt9rs/new_to_zig_i_had_some_questions_and_comments/" text="New to Zig. I had some questions and comments" />

</v-click>

<!--
Operator overloading can be very useful, but there is often a concern that it hinders the ability to understand code at first glance: not only may you have to check whether + really means add, but it hides a function call. One of Zig's main objectives is clarity, so this makes operator overloading a no-go.
-->
