---
description: Gera um List dentro de uma faixa de valores.
---

# Range

Usando `..` ele cria com **intervalo aberto**.

```kotlin
numbers := 2..5

writeln(numbers)

# Output
> [2, 3, 4]
```

Com `...` ele cria com **intervalo fechado**.

```kotlin
numbers := 2...5

writeln(numbers)

# Output
> [2, 3, 4, 5]
```

Ele também pode ser usado com chars.

```ruby
letters := 'a'...'g'

writeln(numbers)

# Output
> ['a', 'b', 'c', 'd', 'e', 'f', 'g']
```

Pode ser utilizado com o each.

```ruby
range := 2...10

range.each(n => writeln(n))

# Output
> 2
> 3
> 4
> 5
> 6
> 7
> 8
> 9
> 10
```

