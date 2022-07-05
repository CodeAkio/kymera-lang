# LikedList

## Introdução

O `LinkedList` permite armazenar vários valores de diferentes tipos e poderá acessar de forma rápida elementos no início e fim da lista. Esses múltiplos valores são armazenados em uma variável ou uma constante do tipo `LinkedList`.

## Declaração e Atribuição

Pode definir o tipo de variável implicitamente com `l[]`.

```
fruit = l['Apple', 'Orange', 'Banana']
```

Deverá definir o tipo de variável explicitamente como `LinkedList`.

```csharp
LinkedList fruit = ['Apple', 'Orange', 'Banana']
```

Também é possível restringir o tipo de dados que a lista pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.\
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

writeln numbers

# Output
> [1, 2, 3, 4, 5]
```

Também podemos utilizar uma matriz.

```csharp
LinkedList<int> matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

writeln matrix[1][2]

# Output
> 6
```

## Operações

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

numbers = numbers + [6, 7, 8, 9, 10]
writeln numbers

# Output
> [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

numbers = numbers - [2, 4]
writeln numbers

# Output
> [1, 3, 5]
```

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

numbers = numbers * 2
writeln numbers

# Output
> [1, 2, 3, 4, 5, 1, 2, 3, 4, 5]
```

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

writeln(5 in numbers)

# Output
> true
```

## Methods

Uma lista possui vários métodos úteis que podem ser utilizados.

### addFirst

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]
numbers.addFirst(6)

writeln numbers

# Output
> [6, 1, 2, 3, 4, 5]
```

### addLast

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]
numbers.addLast(6)

writeln numbers

# Output
> [1, 2, 3, 4, 5, 6]
```

### addBefore

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]
numbers.addBefore(4, 7)

writeln numbers

# Output
> [1, 2, 3, 7, 4, 5]
```

### addAfter

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]
numbers.addAfter(4, 7)

writeln numbers

# Output
> [1, 2, 3, 4, 7, 5]
```

### remove

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]
numbers.remove(2)

writeln numbers

# Output
> [1, 6, 3, 4, 5]
```

### removeFirst

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]
numbers.removeFirst()

writeln numbers

# Output
> [2, 6, 3, 4, 5]
```

### removeLast

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]
numbers.removeLast()

writeln numbers

# Output
> [1, 2, 6, 3, 4]
```

### reverse

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

writeln numbers.reverse

# Output
> [5, 4, 3, 2, 1]
```

### contains

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

writeln numbers.contains(1)
writeln numbers.contains(6)

# Output
> true
> false
```

### indexOf

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

writeln numbers.indexOf(1)

# Output
> 0
```

### sort

```csharp
LinkedList<int> numbers = [4, 1, 5, 3, 2]

writeln numbers.sort

# Output
> [1, 2, 3, 4, 5]
```

### length

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

writeln numbers.length

# Output
> 5
```

### each

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

numbers.each(number do writeln number)

# Output
> 1
> 2
> 3
> 4
> 5
```

### map

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

var newNumbers = numbers.map(number do number * 2)

writeln newNumbers

# Output
> [2, 4, 6, 8, 10]
```

### find

```csharp
LinkedList<int> numbers = [1, 2, 3, 4, 5]

writeln numbers.find(3)

# Output
> 3
```

```dart
LinkedList<string> colors = ['Red', 'Yellow', 'Blue', 'Orange', 'White']

writeln colors.find(r"[ed]")

# Output
> 'Red'
```

### findAll

```csharp
LinkedList<int> numbers = [6, 2, 8, 3, 6]

writeln numbers.find(6)

# Output
> [6, 6]
```

```csharp
LinkedList<string> colors = ['Red', 'Yellow', 'Blue', 'Orange', 'White']

writeln colors.find(r"[w]")

# Output
> ['Yellow', 'White']
```

### first

```csharp
LinkedList<string> colors = ['Red', 'Yellow', 'Blue', 'Orange', 'White']

writeln colors.first()

# Output
> 'Red'
```

### last

```csharp
LinkedList<string> colors = ['Red', 'Yellow', 'Blue', 'Orange', 'White']

writeln colors.last()

# Output
> 'White'
```

### max

```csharp
LinkedList<int> numbers = [6, 2, 8, 3, 6]

writeln numbers.max()

# Output
> 8
```

### min

```csharp
LinkedList<int> numbers = [6, 2, 8, 3, 6]

writeln numbers.min()

# Output
> 2
```

### sum

```csharp
LinkedList<int> numbers = [6, 2, 8, 3, 6]

writeln numbers.sum()

# Output
> 25
```

### avg

```csharp
LinkedList<int> numbers = [6, 2, 8, 3, 6]

writeln numbers.avg()

# Output
> 5
```
