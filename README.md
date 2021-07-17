---
description: Welcome to the kymera-lang!
---

# Welcome

![Chimera Card - Ragnarok](https://camo.githubusercontent.com/3df75fc4d185864d6b8f782d418f2f9a9afc8860/68747470733a2f2f7669676e65747465312e77696b69612e6e6f636f6f6b69652e6e65742f7261676e61726f6b383831322f696d616765732f362f36342f4368696d657261436172642e706e672f7265766973696f6e2f6c61746573743f63623d3230313330323139303030343334)

Kymera lang is a new programming language based on some parts of Python, Ruby, Go, C\#, C, Matlab, Kotlin, Dart and TypeScript.

### Naming

 Kymera is based on word **"Chimera"** that is:

> _"...a mythological, fire-breathing monster, commonly represented with a lion's head, a goat's body, and a serpent's tail."_ [\[1\]](http://www.dictionary.com/browse/chimera)

 Like a chimera, Kymera is created based on some parts of another languages:

* Use the simple syntax and semantics like Python 3.x and Ruby;
* Use Object-oriented programming from C\#;
* Use pointer Go;
* Use .Net Core 2.x to compile like C\#;
* Use parallel programming like Go;
* Use module system like Ruby and Go;
* Use package manager like npm;
* Use matrix operations and other some math methods of matlab;
* Work with text like python and ruby;
* Use braces like C\# to define blocks;
* And other things from this languages.

### Why Kymera?

 It try to join the best of all worlds \(programming languages in this case\), because:

* You write a little and do a lot of things like Pyhton and Ruby, different from java and c\#.
* You have a powerfull language because you can do almost everything you think with standard library or third party packages, and can do what Python 3.x, Ruby, Go, C\#, C, matlab and TypeScript do with Kymera's way.
* We like to do everything in a methodical and organized way. So it can be robust, secure, documented and standardized.
* The error message is clear, and you don't need to use the stackoverflow to understand this messages.
* Use OOP like C\# and Java.
* Features of new programming languages.
* Best practices are implemented by default, like implicit void return to function, private atributes to objects and public methods of objects.
* Write code with a flexible syntax. For example, declaration of variable types and access modifiers is optional.
* You can use in several things: Create console code, desktop GUI aplications, web sites, REST API, mobile apps, games, web scraping, AI, pentest, computer forensics, network applications and other things.

### Features

* General-purpose programming language
* Implemented on all major platforms
* Garbage collection

### Philosophy

Kymera use python \([PEP 20](https://en.wikipedia.org/wiki/Zen_of_Python)\) and ruby on rails \([DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) and [CoC](https://en.wikipedia.org/wiki/Convention_over_configuration)\) philosophy.

Besides these philosophies, Kymera uses some of the [Unix Philosophy](https://en.wikipedia.org/wiki/Unix_philosophy) below:

**Note:** In some cases, replace the word 'program' by module or package.

* Write programs that do one thing and do it well.
* Write programs to work together.
* Small is beautiful.
* Build a prototype as soon as possible.
* Choose portability over efficiency.
* Rule of Modularity.
* Rule of Composition.
* Rule of Separation.
* Rule of Simplicity.
* Rule of Parsimony.
* Rule of Transparency.
* Rule of Robustness.
* Rule of Representation.
* Rule of Least Surprise.
* Rule of Silence.
* Rule of Repair.
* Rule of Economy.
* Rule of Generation.
* Rule of Optimization.
* Rule of Extensibility.

Kymera also has its own philosophy:

* Ever use Kymera design pattern.
* Stop to use Java now.
* Do more, write less.
* Make Kymera very secure and speed.
* Make standard library rich.
* Just import modules that you really need.
* Help us to make it a very good language.
* Play Ragnarok.

### Uses

 As it works with .Net Core, the Kymera can run in windows, linux and mac os.

### Sample code

```text
package main

from standard import *

class Post(
    id int,
    author String,
    title String,
    body String
) {}

main() {
    post = Post(
        0,
        'Chewbacca',
        'Programming language',
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit...'
    )

    writeln("The title is: ${post.title}.")
    writeln("The author is: ${post.author}.")

    writeln("The body before: ${post.body}")

    post.body = "Sed pharetra turpis vehicula orci sodales, interdum blandit libero scelerisque."
    writeln("The body after: ${post.body}")
}

# The output
> The title is: Programming language.
> The author is: Chewbacca
> The body before: Lorem ipsum dolor sit amet, consectetur adipiscing elit...
> The body after: Sed pharetra turpis vehicula orci sodales, interdum blandit libero scelerisque.
```



