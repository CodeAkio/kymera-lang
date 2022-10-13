# Queue

## Introdução

O `Queue` permite armazenar vários valores de diferentes tipos em uma estrutura **FIFO**.

## Declaração e Atribuição

Pode definir o tipo de variável implicitamente com `q[]`.

```python
fruit = q["Apple", "Orange", "Banana"]
```

Deverá definir o tipo de variável explicitamente como `Queue`.

```csharp
fruit Queue = ["Apple", "Orange", "Banana"]
```

Também é possível restringir o tipo de dados que a fila pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.\
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

```csharp
numbers Queue<int> = [1, 2, 3, 4, 5]

writeln(numbers)

# q[1, 2, 3, 4, 5]
```

Também podemos utilizar uma matriz.

```csharp
matrix Queue<Queue<int>> = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

writeln(matrix[1][2])

# 6
```

## Operações

```csharp
numbers Queue<int> = [1, 2, 3, 4, 5]

numbers = numbers + [6, 7, 8, 9, 10]
writeln(numbers)

# q[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

```csharp
numbers Queue<int> = [1, 2, 3, 4, 5]

numbers = numbers - [2, 4]
writeln(numbers)

# q[1, 3, 5]
```

```csharp
numbers Queue<int> = [1, 2, 3, 4, 5]

numbers = numbers * 2
writeln(numbers)

# q[1, 2, 3, 4, 5, 1, 2, 3, 4, 5]
```

## Methods

Uma fila possui vários métodos úteis que podem ser utilizados.

### enqueue

```csharp
numbers Queue<int> = [1, 2, 3, 4, 5]
numbers.enqueue(6)

writeln(numbers)

# q[1, 2, 3, 4, 5, 6]
```

### dequeue

```csharp
numbers Queue<int> = [1, 2, 3, 4, 5]
numbers.dequeue()

writeln(numbers)

# q[2, 6, 3, 4, 5]
```

### reverse

```csharp
numbers Queue<int> = [1, 2, 3, 4, 5]

writeln(numbers.reverse())

# q[5, 4, 3, 2, 1]
```

### sort

```csharp
numbers Queue<int> = [4, 1, 5, 3, 2]

writeln(numbers.sort())

# q[1, 2, 3, 4, 5]
```

### length

```csharp
numbers Queue<int> = [1, 2, 3, 4, 5]

writeln(numbers.length())

# 5
```

### each

```csharp
numbers Queue<int> = [1, 2, 3, 4, 5]

numbers.each(number => writeln(number))

# 1
# 2
# 3
# 4
# 5
```

### map

```csharp
numbers Queue<int> = [1, 2, 3, 4, 5]

var newNumbers = numbers.map(number => number * 2)

writeln(newNumbers)

# q[2, 4, 6, 8, 10]
```

### sum

```csharp
numbers Queue<int> = [6, 2, 8, 3, 6]

writeln(numbers.sum())

# 25
```

### avg

```csharp
numbers Queue<int> = [6, 2, 8, 3, 6]

writeln(numbers.avg())

# 5
```
