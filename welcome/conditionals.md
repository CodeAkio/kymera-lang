# Conditionals

## if

```text
if [declaration]; <expression> {
    <commands>
}
```

```go
if 10 > 1 {
  write('10 é maior')
}
```

```go
if x := 10; x > 1 {
  write('x é maior que 1')
}
```

## else

```text

if [declaration]; <expression> {
    <commands>
} else {
    <commands>
}
```

```go
if 10 > 1 {
  write('10 é maior')
} else {
  write('10 não é maior')
}
```

## else if

```text

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

## Ternary if

```text
<variable or constant> = <expression> ? <command 1> : <command 2>
```

## Switch

```text
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
x := 4
y := 5

switch {
    case isOdd(x):
        writeln('x is odd')
    case isEven(y):
        writeln('y is even')
    default:
        writeln('Something')
}
```

