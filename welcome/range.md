---
description: Gera um List dentro de uma faixa de valores.
---

# Range

Com `..` ele cria com **intervalo fechado**.

```kotlin
var numbers = 2..5

writeln(numbers)

# [2, 3, 4, 5]
```

Usando `..<` ele cria com **intervalo aberto**.

```kotlin
var numbers = 2..<5

writeln(numbers)

# [2, 3, 4]
```

Ele também pode ser usado com strings.

```kotlin
var letters = "a".."g"

writeln(numbers)

# ["a", "b", "c", "d", "e", "f", "g"]
```

Pode ser utilizado com o each.

```kotlin
var range = 2..10

range.each(n => writeln(n))

# 2
# 3
# 4
# 5
# 6
# 7
# 8
# 9
# 10
```

Podemos usar o `step` para definir de quanto em quanto ele **pula**:

```kotlin
var numbers = [1..10].step(2)

writeln(numbers)

# [1, 3, 5, 7, 9]
```

Também existe a função `range` que faz tudo acima:

```kotlin
# intervalo fechado

var numbers = range(from: 2, to: 5)

writeln(numbers)

# [2, 3, 4, 5]
```

```kotlin
# intervalo aberto

var numbers = range(from: 2, until: 5)

writeln(numbers)

# [2, 3, 4]
```

```kotlin
var numbers = range(from: 1, to: 10, step: 2)

writeln(numbers)

# [1, 3, 5, 7, 9]
```
