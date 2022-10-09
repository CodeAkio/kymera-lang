# Stack

## Introdução

O `Stack` permite armazenar vários valores de diferentes tipos em uma estrutura **LIFO**.

## Declaração e Atribuição

Pode definir o tipo de variável implicitamente com `stack[]`.

```python
fruit = stack["Apple", "Orange", "Banana"]
```

Deverá definir o tipo de variável explicitamente como `Stack`.

```csharp
Stack fruit = ["Apple", "Orange", "Banana"]
```

Também é possível restringir o tipo de dados que a pilha pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.\
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

```csharp
Stack<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers)

# stack[1, 2, 3, 4, 5]
```

Também podemos utilizar uma matriz.

```csharp
Stack<int> matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

writeln(matrix[1][2])

# 6
```

## Operações

```csharp
Stack<int> numbers = [1, 2, 3, 4, 5]

numbers = numbers + [6, 7, 8, 9, 10]
writeln(numbers)

# stack[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

```csharp
Stack<int> numbers = [1, 2, 3, 4, 5]

numbers = numbers - [2, 4]
writeln(numbers)

# stack[1, 3, 5]
```

```csharp
Stack<int> numbers = [1, 2, 3, 4, 5]

numbers = numbers * 2
writeln(numbers)

# stack[1, 2, 3, 4, 5, 1, 2, 3, 4, 5]
```

## Methods

Uma pilha possui vários métodos úteis que podem ser utilizados.

### push

```csharp
Stack<int> numbers = [1, 2, 3, 4, 5]
numbers.push(6)

writeln(numbers)

# stack[1, 2, 3, 4, 5, 6]
```

### pop

```csharp
Stack<int> numbers = [1, 2, 3, 4, 5]
numbers.pop()

writeln(numbers)

# stack[1, 2, 6, 3, 4]
```

### reverse

```csharp
Stack<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.reverse)

# stack[5, 4, 3, 2, 1]
```

### sort

```csharp
Stack<int> numbers = [4, 1, 5, 3, 2]

writeln(numbers.sort)

# stack[1, 2, 3, 4, 5]
```

### length

```csharp
Stack<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.length)

# 5
```

### each

```csharp
Stack<int> numbers = [1, 2, 3, 4, 5]

numbers.each(number => writeln(number))

# 1
# 2
# 3
# 4
# 5
```

### map

```csharp
Stack<int> numbers = [1, 2, 3, 4, 5]

var newNumbers = numbers.map(number => number * 2)

writeln(newNumbers)

# stack[2, 4, 6, 8, 10]
```

### sum

```csharp
Stack<int> numbers = [6, 2, 8, 3, 6]

writeln(numbers.sum())

# 25
```

### avg

```csharp
Stack<int> numbers = [6, 2, 8, 3, 6]

writeln(numbers.avg())

# 5
```
