---
description: Welcome to the kymera-lang!
---

# Welcome

Kym lang is a new programming language based on some parts of Python 3, Ruby, Elixir, Go, C#, Kotlin, Dart, Julia, Crystal, Nim, Rust and TypeScript.

### Sample code

```kotlin
package main

class Post(
    id int,
    author string,
    title string,
    body string,
) end

fun main()
    var post = Post(
        0,
        "Chewbacca",
        "Programming language",
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit..."
    )

    writeln("The title is: ${post.title}.")
    writeln("The author is: ${post.author}.")
    writeln("The body before: ${post.body}")

    post.body = "Sed pharetra turpis vehicula orci sodales, interdum blandit libero scelerisque."
    writeln("The body after: ${post.body}")
end

# The title is: Programming language.
# The author is: Chewbacca
# The body before: Lorem ipsum dolor sit amet, consectetur adipiscing elit...
# The body after: Sed pharetra turpis vehicula orci sodales, interdum blandit libero scelerisque.
```

