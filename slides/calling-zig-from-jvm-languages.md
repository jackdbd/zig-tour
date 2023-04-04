---
layout: default
---
# Calling Zig from JVM languages

- <Anchor href="https://docs.oracle.com/javase/7/docs/technotes/guides/jni/spec/intro.html" text="Java Native Interface (JNI)" />

The [Android NDK](https://developer.android.com/ndk/guides) uses the JNI. Watch <Anchor href="https://archive.fosdem.org/2021/schedule/event/zig_android/" text="Create an Android Application with Zig" />

- <Anchor href="https://openjdk.org/projects/panama/" text="Project Panama" /> (Java 19+)

The presentation <Anchor 
  href="https://youtu.be/4xFV-A7JToY?t=1228" 
  text="Project Panama: Say Goodbye to JNI"  /> shows both approaches.

- <Anchor href="https://www.graalvm.org/latest/reference-manual/wasm/" text="GraalWasm" /> (GraalVM WASI runtime)

<!-- 
Panama is easier to use and offers a better performance than the JNI.
Also, JNI errors can crash the JVM, while Panama error don't.
-->
