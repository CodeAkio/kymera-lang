---
description: The parenthesis is optional to pass expression.
---

# Conditionals

## if

```go
if <expression> {
    <commands>
}
```

```go
if 10 > 1 {
  writeln('10 é maior')
}
```

Para evitar uma expressão gigante ou um grande encadeamento de ifs e ands, Baseado no with do Elixir, o if permite passar múltiplas expressões separadas por virgula:

```go
const user = User(name: 'Kym', age: 20, payment: :ok)

if isAdult(user.age),
   isDefaulter(user.payment),
{
  writeln('Can access!')
}
```

{% hint style="info" %}
Priorize soluções com múltiplas funções utilizando _patten matching_ e _when_.
{% endhint %}

{% hint style="info" %}
Ao usar este if, é indicado abstrair as expressões utilizando funções que retornam um boolean, assim o código fica mais limpo.
{% endhint %}

## else

```go

if <expression> {
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

## elsif

{% hint style="info" %}
Devido ao **efeito sonoro** e **encurtamento da sintaxe** do _else if_ em uma palavra, adotamos o padrão do _Perl_ de usar o `elsif`.
{% endhint %}

```perl

if <expression> {
    <commands>
} elsif <expression> {
    <commands>
} elsif <expression> {
    <commands>
else {
    <commands>
}
```

```perl
nota := 8.0

if nota >= 9.0 {
    writeln('Excellent')
} elsif nota >= 7.0 and nota < 9.0 {
    writeln('Good')
} elsif nota >= 4.0 and nota < 7.0 {
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
switch <expression>] {
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

