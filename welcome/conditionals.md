---
description: The parenthesis is optional to pass expression.
---

# Conditionals

## if

O `then` é opcional para a abertura de bloco, é indicado utiliza-lo apenas em casos especiais.

```ruby
if <expression> [then]
    <commands>
end
```

```ruby
if 10 > 1
    writeln("10 é maior")
end
```

```ruby
if 2 in (1 to 10)
    writeln("It is in range 1 to 10")
end
```

Para evitar uma expressão gigante ou um grande encadeamento de ifs e ands, baseado no with do Elixir, o if permite passar múltiplas expressões separadas por vírgula.

Nesses caso se deve usar o `then`:

```ruby
var user = User(name: "Kym", age: 20, payment: :ok)

if (isAdult(user.age),
   isDefaulter(user.payment))
then
    writeln('Can access!')
end
```

{% hint style="info" %}
Priorize soluções com múltiplas funções utilizando _patten matching_ e _when_.
{% endhint %}

{% hint style="info" %}
Ao usar este if, é indicado abstrair as expressões utilizando funções que retornam um boolean, assim o código fica mais limpo.
{% endhint %}

## else

```ruby

if <expression> [then]
    <commands>
else
    <commands>
end
```

```ruby
if 10 > 1
  writeln("10 é maior")
else
  writeln("10 não é maior")
end
```

## elsif

{% hint style="info" %}
Devido ao **efeito sonoro** e **encurtamento da sintaxe** do _else if_ em uma palavra, adotamos o padrão do _Ruby_ de usar o `elsif`.
{% endhint %}

```ruby

if <expression>
    <commands>
elsif <expression>
    <commands>
elsif <expression>
    <commands>
else
    <commands>
end
```

```ruby
var nota = 8.0

if nota >= 9.0
    writeln("Excellent")
elsif nota >= 7.0 and nota < 9.0
    writeln("Good")
elsif nota >= 4.0 and nota < 7.0
    writeln("Bad")
else
    writeln("Terrible")
end

# Output
$ "Excellent"
```

## One line if

Não existe if ternário, mas a ideia dele é a mesma usando o `then` e `else`, que é mais compreensível e significativo do que o `?:`.

```ruby
<variable or constant> = if <expression> then <command 1> else <command 2>
```

```ruby
var age = 22

var message = if (age >= 18) then "Is an adult" else "Is not an adult"

writeln(message)

# Output
> "Is an adult"
```

Uma forma mais elegante e mais indicada é quebrando linha:

```ruby
var age = 22

var message = if age >= 18
    then "Is an adult"
    else "Is not an adult"

writeln(message)

# Output
> "Is an adult"
```

Podemos usar apenas o `then` que quando a expressão é verdadeira, ele retorna o valor, caso contrário, devolve `null`.

```ruby
var age = 22

var message = if age >= 18 then "Is an adult"

writeln(message)

# Output
> "Is an adult"
```

```ruby
var age = 17

var message = if age >= 18 then "Is an adult"

writeln(message)

# Output
> null
```

## When

```kotlin
when [<expression>] {
    <value | expression> -> <commands>
    <value | expression> -> <commands>
    <value | expression> -> {
        <commands>
    }
    [else] -> <commands>
}
```

```kotlin
var gender = 1

when gender {
    0 -> writeln("Male")
    1 -> writeln("Female")
    else -> writeln("Other")
}
```

```kotlin
var rate = 4

when {
    rate => 4 -> writeln("Good")
    rate <= 2 -> writeln("Bad")
    rate == 3 -> writeln("Fair")
    else -> writeln("Invalid")
}
```

```kotlin
var x, y = 4, 5

when {
    isOdd(x) -> writeln("x is odd")
    isEven(y) -> writeln("y is even")
}
```

```kotlin
when {
    0, 2, 4, 6, 8 -> writeln("Even")
    1, 3, 5, 7, 9 -> writeln("Odd")
}
```

```kotlin
when {
    1 to 7 -> writeln("Bad")
    7 until 10 -> writeln("Good")
}
```

[https://kotlinlang.org/docs/control-flow.html#when-expression](https://kotlinlang.org/docs/control-flow.html#when-expression)
