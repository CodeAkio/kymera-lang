# LinkedList

## Introdução

O `LinkedList` permite armazenar vários valores de diferentes tipos e poderá acessar de forma rápida elementos no início e fim da lista. Esses múltiplos valores são armazenados em uma variável ou uma constante do tipo `LinkedList`.

## Declaração e Atribuição

Pode definir o tipo de variável implicitamente com `ll[]`, por baixo ele gera um `LinkedList<dyn>`.

```python
fruit = ll["Apple", "Orange", "Banana"]
```



Deverá definir o tipo de variável explicitamente como `LinkedList`.

```csharp
fruit LinkedList = ["Apple", "Orange", "Banana"]
```



Também é possível restringir o tipo de dados que a lista pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.\
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]

writeln(numbers)

# ll[1, 2, 3, 4, 5]
```



Também podemos utilizar uma matriz.

```csharp
matrix LinkedList<LinkedList<int>> = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

writeln(matrix[1][2])

# 6
```

## Operações

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]

numbers = numbers + [6, 7, 8, 9, 10]
writeln(numbers)

# ll[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]

numbers = numbers - [2, 4]
writeln(numbers)

# ll[1, 3, 5]
```

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]

numbers = numbers * 2
writeln(numbers)

# ll[1, 2, 3, 4, 5, 1, 2, 3, 4, 5]
```

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]

writeln(5 in numbers)

# true
```

## Methods

Uma lista possui vários métodos úteis que podem ser utilizados.

### addFirst

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]
numbers.addFirst(6)

writeln(numbers)

# ll[6, 1, 2, 3, 4, 5]
```

### addLast

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]
numbers.addLast(6)

writeln(numbers)

# ll[1, 2, 3, 4, 5, 6]
```

### addBefore

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]
numbers.addBefore(4, 7)

writeln(numbers)

# ll[1, 2, 3, 7, 4, 5]
```

### addAfter

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]
numbers.addAfter(4, 7)

writeln(numbers)

# ll[1, 2, 3, 4, 7, 5]
```

### remove

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]
numbers.remove(2)

writeln(numbers)

# ll[1, 6, 3, 4, 5]
```

### removeFirst

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]
numbers.removeFirst()

writeln(numbers)

# ll[2, 6, 3, 4, 5]
```

### removeLast

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]
numbers.removeLast()

writeln(numbers)

# ll[1, 2, 6, 3, 4]
```

### reverse

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]

writeln(numbers.reverse())

# ll[5, 4, 3, 2, 1]
```

### contains

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]

writeln(numbers.contains(1))
writeln(numbers.contains(6))

# true
# false
```

### indexOf

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]

writeln(numbers.indexOf(1))

# 0
```

### sort

```csharp
numbers LinkedList<int> = [4, 1, 5, 3, 2]

writeln(numbers.sort())

# ll[1, 2, 3, 4, 5]
```

### length

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]

writeln(numbers.length())

# 5
```

### each

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]

numbers.each(number => writeln(number))

# 1
# 2
# 3
# 4
# 5
```

### map

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]

var newNumbers = numbers.map(number => number * 2)

writeln(newNumbers)

# ll[2, 4, 6, 8, 10]
```

### find

```csharp
numbers LinkedList<int> = [1, 2, 3, 4, 5]

writeln(numbers.find(3))

# 3
```

```csharp
colors LinkedList<string> = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.find(r"[ed]"))

# "Red"
```

### findAll

```csharp
numbers LinkedList<int> = [6, 2, 8, 3, 6]

writeln(numbers.find(6))

# ll[6, 6]
```

```csharp
colors LinkedList<string> = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.find(r"[w]"))

# ll["Yellow", "White"]
```

### first

```csharp
colors LinkedList<string> = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.first())

# "Red"
```

### last

```csharp
colors LinkedList<string> = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.last())

# "White"
```

### max

```csharp
numbers LinkedList<int> = [6, 2, 8, 3, 6]

writeln(numbers.max())

# 8
```

### min

```csharp
numbers LinkedList<int> = [6, 2, 8, 3, 6]

writeln(numbers.min())

# 2
```

### sum

```csharp
numbers LinkedList<int> = [6, 2, 8, 3, 6]

writeln(numbers.sum())

# 25
```

### avg

```csharp
numbers LinkedList<int> = [6, 2, 8, 3, 6]

writeln(numbers.avg())

# 5
```

### uniq

Força cada elemento da lista a ser único.

```csharp
numbers LinkedList<int> = [6, 2, 8, 3, 6]

writeln(numbers.uniq())

# ll[6, 2, 8, 3]
```
