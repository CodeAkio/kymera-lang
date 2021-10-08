# Queue

## Introdução

O `Queue` permite armazenar vários valores de diferentes tipos em uma estrutura **FIFO**.

## Declaração e Atribuição

Deverá definir o tipo de variável explicitamente como `Queue`.

```csharp
Queue fruit = ['Apple', 'Orange', 'Banana']
```

Também é possível restringir o tipo de dados que a fila pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.  
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

```csharp
Queue<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers)

# Output
> [1, 2, 3, 4, 5]
```

Também podemos utilizar uma matriz.

```csharp
Queue<int> matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

writeln(matrix[1][2])

# Output
> 6
```

## Operações

```csharp
Queue<int> numbers = [1, 2, 3, 4, 5]

numbers = numbers + [6, 7, 8, 9, 10]
writeln(numbers)

# Output
> [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

```csharp
Queue<int> numbers = [1, 2, 3, 4, 5]

numbers = numbers - [2, 4]
writeln(numbers)

# Output
> [1, 3, 5]
```

```csharp
Queue<int> numbers = [1, 2, 3, 4, 5]

numbers = numbers * 2
writeln(numbers)

# Output
> [1, 2, 3, 4, 5, 1, 2, 3, 4, 5]
```

## Methods

Uma fila possui vários métodos úteis que podem ser utilizados.

### enqueue

```csharp
Queue<int> numbers = [1, 2, 3, 4, 5]
numbers.enqueue(6)

writeln(numbers)

# Output
> [1, 2, 3, 4, 5, 6]
```

### dequeue

```csharp
Queue<int> numbers = [1, 2, 3, 4, 5]
numbers.dequeue()

writeln(numbers)

# Output
> [2, 6, 3, 4, 5]
```

### reverse

```csharp
Queue<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.reverse)

# Output
> [5, 4, 3, 2, 1]
```

### sort

```csharp
Queue<int> numbers = [4, 1, 5, 3, 2]

writeln(numbers.sort)

# Output
> [1, 2, 3, 4, 5]
```

### length

```csharp
Queue<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.length)

# Output
> 5
```

### each

```csharp
Queue<int> numbers = [1, 2, 3, 4, 5]

numbers.each(number => writeln(number))

# Output
> 1
> 2
> 3
> 4
> 5
```

### map

```csharp
Queue<int> numbers = [1, 2, 3, 4, 5]

newNumbers := numbers.map(number => number * 2)

writeln(newNumbers)

# Output
> [2, 4, 6, 8, 10]
```

### sum

```csharp
Queue<int> numbers = [6, 2, 8, 3, 6]

writeln(numbers.sum())

# Output
> 25
```

### avg

```csharp
Queue<int> numbers = [6, 2, 8, 3, 6]

writeln(numbers.avg())

# Output
> 5
```

