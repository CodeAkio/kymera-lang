---
description: Syntax and semantics of variables and constants
---

# Variable and Constant

## Variables

The variables work with optional typing similar to TypeScript and Go, but with the possibility to use the types available through C\# language.

You need to use **var** keyword to declare a variable.

### Declaration and Assignment

 **Syntax:**

```text
# With type definition
<variable_name> [type] = <value>

# With type inference
<variable_name> := <value>

# Assignment value after declaration
<variable_name> = <value>
```

**Sample:**

```go
number int = 10
write(number)

animal := "Dog"
write(animal)

animal = "Cat"
write(animal)

# Output
> 10
> "Dog"
> "Cat"
```

## Constants

Constants need to be declared with the keyword **const** and have **uppercase** name.

**Syntaxe:**

```text
const <CONSTANT_NAME> := <value>
```

**Sample:**

```text
const PI := 3.141592653589793
```

