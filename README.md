---
description: Welcome to the kim-lang!
---

# Welcome

Kim lang é um protótipo de uma nova linguagem de programação brasileira que usa como base outras linguagens como: Python 3, Ruby, Elixir, Go, Kotlin, Dart, Julia, Crystal, Nim, Rust, Swift e TypeScript.

```csharp
package main

struct Post {
    id     int
    author string
    title  string
    body   string
}

fun main() {
    var post = Post(0,
                    "Chewbacca",
                    "Programming language",
                    "Lorem ipsum dolor sit amet, consectetur adipiscing elit...")

    writeln("The title is: ${post.title}
            The author is: ${post.author}
            The body before: ${post.body}")

    post.body = "Sed pharetra turpis vehicula orci sodales, interdum blandit libero scelerisque."
    writeln("The body after: ${post.body}")
}
```

```ruby
# The title is: Programming language
# The author is: Chewbacca
# The body before: Lorem ipsum dolor sit amet, consectetur adipiscing elit...
# The body after: Sed pharetra turpis vehicula orci sodales, interdum blandit libero scelerisque.
```
