---
description: Syntax and semantics of variables and constants
---

# Variable and Constant

## Variables

The variables work with optional typing similar to TypeScript and Go, but with the possibility to use the types available through C\# language.

### Declaration and Assignment

 **Syntax:**

```text
# With type definition
[type] <variable name> = <value>

# Without type definition
<variable name> := <value>

# Assignment value after declaration
<variable name> = <value>
```

**Sample:**

```text
int number = 10
write(number)

animal := 'Dog'
write(animal)

animal = 'Cat'
write(animal)

# Output
> 10
> 'Dog'
> 'Cat'
```

## Constants

In Kymera constants can be declared explicitly with the keyword **const** than most languages.

**Syntaxe:**

```text
const PI = <value>
```

**Sample:**

```text
const PI = 3.141592653589793
```

or implicit form using a word that start with uppercase like Ruby Lang.

**Note:** We recommend that all characters must be in the upper case.

**Syntaxe:**

```text
<CONSTANT NAME WITH UPPERCASE> = <value>
```

**Sample:**

```text
PI = 3.141592653589793
```

