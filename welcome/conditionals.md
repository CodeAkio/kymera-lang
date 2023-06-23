---
description: The parenthesis is optional to pass expression.
---

# Conditionals \[WIP]

## if

```ruby
if <expression> {
    <commands>
}
```

```ruby
if 10 > 1 {
    writeln("10 é maior")
}
```

```kotlin
if 2 in 1..10 {
    writeln("It is in range 1 to 10")
}
```



Para evitar uma expressão gigante ou um grande encadeamento de ifs e ands, baseado no with do Elixir, o if permite passar múltiplas expressões separadas por vírgula.

```go
let user = User(name: "Kym", age: 20, payment: :ok)

if (isAdult(user.age),
   isDefaulter(user.payment)) {
   writeln("Can access!")
}
```

{% hint style="info" %}
Priorize soluções com múltiplas funções utilizando _patten matching_ e _when_.
{% endhint %}

{% hint style="info" %}
Ao usar este if, é indicado abstrair as expressões utilizando funções que retornam um boolean, assim o código fica mais limpo.
{% endhint %}

## else

```ruby

if <expression> {
    <commands>
} else {
    <commands>
}
```

```go
if 10 > 1 {
  writeln("10 é maior")
} else {
  writeln("10 não é maior")
}
```

## elsif

{% hint style="info" %}
Devido ao **efeito sonoro** e **encurtamento da sintaxe** do _else if_ em uma palavra, adotamos o padrão do _Ruby_ de usar o `elsif`.
{% endhint %}

```ruby

if <expression> {
    <commands>
} elsif <expression> {
    <commands>
} elsif <expression> {
    <commands>
} else {
    <commands>
}
```

<pre class="language-ruby"><code class="lang-ruby">let nota = 8.0

if nota >= 9.0 {
    writeln("Excellent")
} elsif nota >= 7.0 and nota &#x3C; 9.0 {
    writeln("Good")
<strong>} elsif nota >= 4.0 and nota &#x3C; 7.0 {
</strong>    writeln("Bad")
} else {
    writeln("Terrible")
}

# "Excellent"
</code></pre>

## One line if

Não existe if ternário, mas a ideia dele é a mesma usando o `then` e `else`, que é mais compreensível e significativo do que o `?:`.

```ruby
<variable or constant> = if <expression> then <command 1> else <command 2>
```

<pre class="language-ruby"><code class="lang-ruby">let age = 22
<strong>let message = if (age >= 18) then "Is an adult" else "Is not an adult"
</strong>
writeln(message)

# "Is an adult"
</code></pre>

Uma forma mais elegante e mais indicada é quebrando linha:

```ruby
let age = 22

let message = if age >= 18
    then "Is an adult"
    else "Is not an adult"

writeln(message)

# "Is an adult"
```

Podemos usar apenas o `then` que quando a expressão é verdadeira, ele retorna o valor, caso contrário, devolve `null`.

```ruby
let age = 22
let message = if age >= 18 then "Is an adult"

writeln(message)

# "Is an adult"
```

```ruby
let age = 17
let message = if age >= 18 then "Is an adult"

writeln(message)

# null
```

## When

Usamos o `_` quando não queremos armazenar o valor em uma variável.

```kotlin
when [<expression>] {
    <value | expression> -> <commands>
    <value | expression> -> <commands>
    <value | expression> ->
        <commands>
    _ -> <commands>
}
```

```kotlin
let gender = 1

when gender {
    0 -> writeln("Male")
    1 -> writeln("Female")
    _ -> writeln("Other")
}
```

```kotlin
let rate = 4

when {
    rate => 4 -> writeln("Good")
    rate <= 2 -> writeln("Bad")
    rate == 3 -> writeln("Fair")
    _ -> writeln("Invalid")
}
```

```kotlin
let x, y = 4, 5

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
    1..7 -> writeln("Bad")
    7..<10 -> writeln("Good")
}
```

[https://kotlinlang.org/docs/control-flow.html#when-expression](https://kotlinlang.org/docs/control-flow.html#when-expression)
