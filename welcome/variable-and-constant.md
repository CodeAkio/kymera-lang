---
description: Syntax and semantics of variables and constants
---

# Variable

The variables work with optional typing similar to TypeScript and Go, but with the possibility to use the types available through C# language.

&#x20;**Syntax:**

```go
# With type definition
<variable_name> <type> = <value>

# With type inference
var <variable_name> = <value>

# Assignment value after declaration
<variable_name> = <value>
```

**Sample:**

```go
number int = 10
writeln(number)
# 10

var animal = "Dog"
writeln(animal)
# "Dog"

animal = "Cat"
writeln(animal)
# "Cat"
```

Também pode usar a declaração curta com (`:=`):

```go
animal := "Cat"
writeln(animal)
# "Cat"
```
