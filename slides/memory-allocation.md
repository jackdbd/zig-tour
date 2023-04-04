# Memory allocation

Esempio di GObject e cairo. Ecco perche' secondo me e' meglio che la memory allocation sia esplicita in un low level language.

Good course on <Anchor 
  href="https://dmitrysoshnikov.teachable.com/p/essentials-of-garbage-collectors" 
  text="Garbage Collection Algorithms — Dmitry Soshnikov" 
  alt="course on garbage collection algorithms by Dmitry Soshnikov" />.

<Quote 
  text="When, how, and whether garbage collection occurs is down to the implementation of any given JavaScript engine. Any behavior you observe in one engine may be different in another engine, in another version of the same engine, or even in a slightly different situation with the same version of the same engine." 
  citeHref="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/FinalizationRegistry"
  citeText="FinalizationRegistry on mdn web docs" />

In Rust c’e’ ma e’ una knightly. [^1]

<Anchor 
  href="https://doc.rust-lang.org/std/alloc/trait.Allocator.html" 
  text="Trait std::alloc::Allocator" 
  alt="Trait std::alloc::Allocator in the Rust documentation" />

Jorge Rodriguez's <Anchor 
  href="https://youtu.be/c0g3S_2QxWM" 
  text="Code for Game Developers - Anatomy of a Memory Allocation" 
  alt="Code for Game Developers - Anatomy of a Memory Allocation on YouTube" />.

Casey Muratori's <Anchor 
  href="https://youtu.be/MvDUe2evkHg" 
  text="Introduction to General Purpose Allocation" 
  alt="Introduction to General Purpose Allocation on YouTube" />. At 27:45 he starts implementing an arena allocator.

[^1]: [This slide is not endorsed by the Rust Foundation](https://twitter.com/rust_foundation/status/1644132378858729474)