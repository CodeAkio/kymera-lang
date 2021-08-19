---
description: The parenthesis is optional to pass expression.
---

# Conditionals

## if

```go
if [declaration]; <expression> {
    <commands>
}
```

```go
if 10 > 1 {
  writeln('10 é maior')
}
```

```go
if x := 10; x > 1 {
  writeln('x é maior que 1')
}
```

## else

```go

if [declaration]; <expression> {
    <commands>
} else {
    <commands>
}
```

```go
if 10 > 1 {
  writeln('10 é maior')
} else {
  writeln('10 não é maior')
}
```

## else if

```go

if <expression> {
    <commands>
} else if <expression> {
    <commands>
} else if <expression> do
    <commands>
else {
    <commands>
}
```

```go
nota := 8.0

if nota >= 9.0 {
    writeln('Excellent')
} else if nota >= 7.0 and nota < 9.0 {
    writeln('Good')
} else if nota >= 4.0 and nota < 7.0 do
    writeln('Bad')
else {
    writeln('Terrible')
}

# Output
> 'Excellent'
```

## Ternary if

```javascript
<variable or constant> = <expression> ? <command 1> : <command 2>
```

```csharp
age := 22

string message = age >= 18 ? 'Is an adult' : 'Is not an adult'

writeln(message)

# Output
> 'Is an adult'
```

## Switch

```csharp
switch [[declaration]; <expression>] {
    case <value>:
        <commands>
    case <value>:
        <commands>
    case <value>:
        <commands>
    default:
        <commands>
}
```

```go
gender := 1

switch gender {
    case 0:
        writeln('Male')
    case 1:
        writeln('Female')
    default:
        writeln('Other')
}
```

```go
switch gender := 1; gender {
    case 0:
        writeln('Male')
    case 1:
        writeln('Female')
    default:
        writeln('Other')
}
```

```go
rate := 4

switch {
    case rate => 4:
        writeln('Good')
    case rate <= 2:
        writeln('Bad')
    case rate == 3:
        writeln('Fair')
    default:
        writeln('Invalid')
}
```

```go
x, y := 4, 5

switch {
    case isOdd(x):
        writeln('x is odd')
    case isEven(y):
        writeln('y is even')
    default:
        writeln('Something')
}
```

