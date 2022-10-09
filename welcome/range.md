---
description: Gera um List dentro de uma faixa de valores.
---

# Range

Usando `until` ele cria com **intervalo aberto**.

```kotlin
var numbers = 2 until 5

writeln(numbers)

# [2, 3, 4]
```

Com `to` ele cria com **intervalo fechado**.

```kotlin
var numbers = 2 to 5

writeln(numbers)

# [2, 3, 4, 5]
```

Ele também pode ser usado com chars.

```kotlin
var letters = 'a' to 'g'

writeln(numbers)

# ['a', 'b', 'c', 'd', 'e', 'f', 'g']
```

Pode ser utilizado com o each.

```kotlin
var range = 2 to 10

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
var numbers = 1 to 10 step 2

writeln(numbers)

# [1, 3, 5, 7, 9]
```
