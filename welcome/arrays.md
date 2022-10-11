---
description: Como utilizar a interface IList
---

# List

## Introdução

O `List` permite armazenar vários valores de diferentes tipos que podem ser acessados através de um índice número que começa com o número 0. Esses múltiplos valores são armazenados em uma variável ou uma constante do tipo `List`.

## Declaração e Atribuição

A declaração de uma variável ou constante List pode ser feito de forma duas formas

* **Explícita:** Deverá definir o tipo de variável explicitamente como List.

```swift
fruit List = ["Apple", "Orange", "Banana"]
```

* **Implícita:** Basta atribuir diretamente os valores a variável e o interpretador vai declara-lo implicitamente como `List<dynamic>`, sendo que os valores ficaram dentro dos colchetes e separados por vírgula.

```go
var fruit = ["Apple", "Orange", "Banana"]
```



Também é possível restringir o tipo de dados que a lista pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.\
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

```swift
numbers List<int> = [1, 2, 3, 4, 5]

writeln(numbers)

# [1, 2, 3, 4, 5]
```



Existe a forma enxuta que é passando o **tipo dos valores** seguido de `[]`.

```csharp
numbers int[] = [1, 2, 3, 4, 5]

writeln(numbers)

# [1, 2, 3, 4, 5]
```



Também podemos utilizar uma matriz.

```csharp
matrix List<int[]> = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

writeln(matrix[1][2])

# 6
```

## Referência de Valores

```csharp
numbers int[] = [1, 2, 3, 4, 5]

writeln(numbers[1])

# 2
```

```csharp
numbers int[] = [1, 2, 3, 4, 5]

numbers[2] = 7

writeln(numbers)

# [1, 2, 7, 4, 5]
```

## Slice

Cria uma novo List baseado em partes de outro List.

```csharp
numbers int[] = [1, 2, 3, 4, 5]

writeln(numbers[2:3])

# [3, 4]
```

```csharp
numbers int[] = [1, 2, 3, 4, 5]

writeln(numbers[:])

# [1, 2, 3, 4, 5]
```

```csharp
numbers int[] = [1, 2, 3, 4, 5]

writeln(numbers[:2])

# [1, 2, 3]
```

```csharp
numbers int[] = [1, 2, 3, 4, 5]

writeln(numbers[2:])

# [3, 4, 5]
```

## Operações

```csharp
var numbers = [1, 2, 3, 4, 5]

numbers = numbers + [6, 7, 8, 9, 10]
writeln(numbers)

# [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

```csharp
var numbers = [1, 2, 3, 4, 5]

numbers = numbers - [2, 4]
writeln(numbers)

# [1, 3, 5]
```

```csharp
var numbers = [1, 2, 3, 4, 5]

numbers = numbers * 2
writeln(numbers)

# [1, 2, 3, 4, 5, 1, 2, 3, 4, 5]
```

```csharp
var numbers = [1, 2, 3, 4, 5]

writeln(5 in numbers)

# true
```

## Methods

Uma lista possui vários métodos úteis que podem ser utilizados.

### add

```csharp
numbers int[] = [1, 2, 3, 4, 5]
numbers.add(6)

writeln(numbers)

# [1, 2, 3, 4, 5, 6]
```

### insert

```csharp
numbers int[] = [1, 2, 3, 4, 5]
numbers.insert(6, 2)

writeln(numbers)

# [1, 2, 6, 3, 4, 5]
```

### remove

```csharp
numbers int[] = [1, 2, 3, 4, 5]
numbers.remove(2)

writeln(numbers)

# [1, 6, 3, 4, 5]
```

### pop

```csharp
numbers int[] = [1, 2, 3, 4, 5]
numbers.pop()

writeln(numbers)

# [1, 2, 6, 3, 4]
```

### reverse

```csharp
numbers int[] = [1, 2, 3, 4, 5]

writeln(numbers.reverse())

# [5, 4, 3, 2, 1]
```

### contains

```csharp
numbers int[] = [1, 2, 3, 4, 5]

writeln(numbers.contains(1))
writeln(numbers.contains(6))

# true
# false
```

### indexOf

```csharp
numbers int[] = [1, 2, 3, 4, 5]

writeln(numbers.indexOf(1))

# 0
```

### sort

```csharp
numbers int[] = [4, 1, 5, 3, 2]

writeln(numbers.sort())

# [1, 2, 3, 4, 5]
```

### length

```csharp
numbers int[] = [1, 2, 3, 4, 5]

writeln(numbers.length())

# 5
```

### each

```csharp
numbers int[] = [1, 2, 3, 4, 5]

numbers.each(number => writeln(number))

# 1
# 2
# 3
# 4
# 5
```

### map

```csharp
numbers int[] = [1, 2, 3, 4, 5]

var newNumbers = numbers.map(number => number * 2)

writeln(newNumbers)

# [2, 4, 6, 8, 10]
```

### find

```csharp
numbers int[] = [1, 2, 3, 4, 5]

writeln(numbers.find(3))

# 3
```

```csharp
colors string[] = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.find(r"[ed]"))

# "Red"
```

### findAll

```csharp
numbers int[] = [6, 2, 8, 3, 6]

writeln(numbers.find(6))

# [6, 6]
```

```csharp
colors string[] = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.find(r"[w]"))

# ["Yellow", "White"]
```

### first

```csharp
colors string[] = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.first())

# "Red"
```

### last

```csharp
colors string[] = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.last())

# "White"
```

### sample

Pega aleatoriamente um item da lista.

```csharp
colors string[] = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.sample())

# "Yellow"
```

### max

```csharp
numbers int[] = [6, 2, 8, 3, 6]

writeln(numbers.max())

# 8
```

### min

```csharp
numbers int[] = [6, 2, 8, 3, 6]

writeln(numbers.min())

# 2
```

### sum

```csharp
numbers int[] = [6, 2, 8, 3, 6]

writeln(numbers.sum())

# 25
```

### avg

```csharp
numbers int[] = [6, 2, 8, 3, 6]

writeln(numbers.avg())

# 5
```
