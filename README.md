---
description: Welcome to the kymera-lang!
---

# Welcome

![Chimera Card - Ragnarok](https://camo.githubusercontent.com/3df75fc4d185864d6b8f782d418f2f9a9afc8860/68747470733a2f2f7669676e65747465312e77696b69612e6e6f636f6f6b69652e6e65742f7261676e61726f6b383831322f696d616765732f362f36342f4368696d657261436172642e706e672f7265766973696f6e2f6c61746573743f63623d3230313330323139303030343334)

Kym lang is a new programming language based on some parts of Python, Ruby, Elixir, Go, C#, Kotlin, Dart and TypeScript.

### Sample code

```go
package main

class Post(
    int id,
    string author,
    string title,
    string body,
)

fun main() {
    post := Post(
        0,
        'Chewbacca',
        'Programming language',
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit...'
    )

    writeln 'The title is: ${post.title}.'
    writeln 'The author is: ${post.author}.'

    writeln 'The body before: ${post.body}'

    post.body = 'Sed pharetra turpis vehicula orci sodales, interdum blandit libero scelerisque.'
    writeln 'The body after: ${post.body}'
}

# The output
> The title is: Programming language.
> The author is: Chewbacca
> The body before: Lorem ipsum dolor sit amet, consectetur adipiscing elit...
> The body after: Sed pharetra turpis vehicula orci sodales, interdum blandit libero scelerisque.
```

### Why Kymera?

&#x20;It try to join the best of all worlds (programming languages in this case), because:

* You write a little and do a lot of things like Pyhton and Ruby, different from java and c#.
* You have a powerfull language because you can do almost everything you think with standard library or third party packages, and can do what Python 3.x, Ruby, Go, C#, C, matlab and TypeScript do with Kymera's way.
* We like to do everything in a methodical and organized way. So it can be robust, secure, documented and standardized.
* The error message is clear, and you don't need to use the stackoverflow to understand this messages.
* Use OOP like C# and Java.
* Features of new programming languages.
* Best practices are implemented by default, like implicit void return to function, private atributes to objects and public methods of objects.
* Write code with a flexible syntax. For example, declaration of variable types and access modifiers is optional.
* You can use in several things: Create console code, desktop GUI aplications, web sites, REST API, mobile apps, games, web scraping, AI, pentest, computer forensics, network applications and other things.

