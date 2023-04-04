# String concatenation

<p>The <code class="inline-code">++</code> and <code class="inline-code">**</code> operators are available <b>only</b> at compile-time.</p>

```
const final_url = "https://github.com/" ++ user ++ "/reponame";
```

<!-- Comptime also introduces the operators ++ and ** for concatenating and repeating arrays and slices. These operators do not work at runtime. Are they syntactic sugar on top of comptime? -->
