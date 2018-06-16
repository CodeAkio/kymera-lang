---
description: Syntax and semantics of Kymera Lang
---

# Syntax and Semantics

## Basic Concepts

### Variables

The variables work with optional typing similar to TypeScript and Go, but with the possibility to use the types available through C\# language.

#### Declaration and Assignment

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

####  Types of scope

Kymera works with three traditional scopes: Global, Block and Function.

#### del

You can use 'del' to remove the variable, constants and objects from memory when you want, this is a cool and flexible Python resource that some other languages haven't. It increase your control, but remember that you have garbage collector to help you.

 **Syntax:**

```text
del <variable | constant | object>
```

 **Sample:**

```text
int number = 10
writeln(number)

del number
writeln(number)

# Output
> 10
> The variable 'b' was not declared.
```

#### null

 To set a variable value as null in some languages, you can do it using the keyword 'nil' \(ruby\) or 'none' \(python\), but it's ugly and not objective, because when you think to set a null value you think in 'null' keyword. So Kymera use the key 'null' like C\# to it.

 **Syntax:**

```text
<variable | constant | object> = null
```

 **Sample:**

```text
int number = 42
writeln(number)

number = null
writeln(number)

# Output
> 42
> null
```

### Console Output

To print something on console you can use the 'Console' class methods, that is 'write' and 'writeln'. This is based on C\#. The 'Console' class can be implicit when you use the syntaxe sugar.

* **Console.write -** Just print a text in your console.
* **Console.writeln -** Print a text in your console and break line.

 **Syntaxe:**

```text
Console.write(<value_to_print>)
Console.writeln(<value_to_print>)
```

 **Syntaxe Sugar:**

```text
write(<value_to_print>)
writeln(<value_to_print>)
```

 **Sample:**

```text
write("Hello ")
write("Universe!")

# Output
> Hello Universe!
```

```text
writeln("Hello ")
writeln("Universe!")

# Output
> Hello 
> Universe!
```

### Console User Input

To print something on console you can use the 'Console' class methods, that is 'read'. This is based on C\#. The 'Console' class can be implicit when you use the syntaxe sugar.

**Syntaxe:**

```text
Console.read
```

**Syntaxe Sugar:**

```text
read
```

 **Sample:**

```text
name = read
write("My name is ${name}")

# Output
> My name is Michael
```

