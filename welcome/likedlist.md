# LinkedList

## Introdução

O `LinkedList` permite armazenar vários valores de diferentes tipos e poderá acessar de forma rápida elementos no início e fim da lista. Esses múltiplos valores são armazenados em uma variável ou uma constante do tipo `LinkedList`.

## Declaração e Atribuição

Pode definir o tipo de variável implicitamente com `l[]`.

```python
fruit = linked["Apple", "Orange", "Banana"]
```

Deverá definir o tipo de variável explicitamente como `LinkedList`.

```csharp
LinkedList fruit = ["Apple", "Orange", "Banana"]
```

Também é possível restringir o tipo de dados que a lista pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.\
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers)

# linked[1, 2, 3, 4, 5]
```

Também podemos utilizar uma matriz.

```csharp
LinkedList<int> matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

writeln(matrix[1][2])

# 6
```

## Operações

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

numbers = numbers + [6, 7, 8, 9, 10]
writeln(numbers)

# linked[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

numbers = numbers - [2, 4]
writeln(numbers)

# linked[1, 3, 5]
```

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

numbers = numbers * 2
writeln(numbers)

# linked[1, 2, 3, 4, 5, 1, 2, 3, 4, 5]
```

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

writeln(5 in numbers)

# true
```

## Methods

Uma lista possui vários métodos úteis que podem ser utilizados.

### addFirst

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]
numbers.addFirst(6)

writeln(numbers)

# linked[6, 1, 2, 3, 4, 5]
```

### addLast

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]
numbers.addLast(6)

writeln(numbers)

# linked[1, 2, 3, 4, 5, 6]
```

### addBefore

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]
numbers.addBefore(4, 7)

writeln(numbers)

# linked[1, 2, 3, 7, 4, 5]
```

### addAfter

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]
numbers.addAfter(4, 7)

writeln(numbers)

# linked[1, 2, 3, 4, 7, 5]
```

### remove

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]
numbers.remove(2)

writeln(numbers)

# linked[1, 6, 3, 4, 5]
```

### removeFirst

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]
numbers.removeFirst()

writeln(numbers)

# linked[2, 6, 3, 4, 5]
```

### removeLast

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]
numbers.removeLast()

writeln(numbers)

# linked[1, 2, 6, 3, 4]
```

### reverse

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.reverse)

# linked[5, 4, 3, 2, 1]
```

### contains

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.contains(1))
writeln(numbers.contains(6))

# true
# false
```

### indexOf

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.indexOf(1))

# 0
```

### sort

```csharp
LinkedList<int> numbers = [4, 1, 5, 3, 2]

writeln(numbers.sort())

# linked[1, 2, 3, 4, 5]
```

### length

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.length)

# 5
```

### each

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

numbers.each(number => writeln(number))

# 1
# 2
# 3
# 4
# 5
```

### map

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

var newNumbers = numbers.map(number => number * 2)

writeln(newNumbers)

# linked[2, 4, 6, 8, 10]
```

### find

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.find(3))

# 3
```

```csharp
LinkedList<String> colors = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.find(r"[ed]"))

# "Red"
```

### findAll

```csharp
LinkedList<int> numbers = [6, 2, 8, 3, 6]

writeln(numbers.find(6))

# linked[6, 6]
```

```csharp
LinkedList<string> colors = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.find(r"[w]"))

# linked["Yellow", "White"]
```

### first

```csharp
LinkedList<string> colors = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.first())

# "Red"
```

### last

```csharp
LinkedList<string> colors = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.last())

# "White"
```

### max

```csharp
LinkedList<int> numbers = [6, 2, 8, 3, 6]

writeln(numbers.max())

# 8
```

### min

```csharp
LinkedList<int> numbers = [6, 2, 8, 3, 6]

writeln(numbers.min())

# 2
```

### sum

```csharp
LinkedList<int> numbers = [6, 2, 8, 3, 6]

writeln(numbers.sum())

# 25
```

### avg

```csharp
LinkedList<int> numbers = [6, 2, 8, 3, 6]

writeln(numbers.avg())

# 5
```
