---
description: Syntax and semantics of variables and constants
---

# Variable and Constant

## Variables

The variables work with optional typing similar to TypeScript and Go, but with the possibility to use the types available through C\# language.

### Declaration and Assignment

 **Syntax:**

```go
# With type definition
[type] <variable_name> = <value>

# With type inference
<variable_name> := <value>

# Assignment value after declaration
<variable_name> = <value>
```

**Sample:**

```go
int number = 10
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

```csharp
const <CONSTANT_NAME> := <value>
const [type] <CONSTANT_NAME> = <value>
```

**Sample:**

```csharp
const PI := 3.141592653589793
const string NAME = "Maria"
```

