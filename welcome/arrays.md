---
description: Como utilizar a interface IList
---

# List

## Introdução

O `List` permite armazenar vários valores de diferentes tipos que podem ser acessados através de um índice número que começa com o número 0. Esses múltiplos valores são armazenados em uma variável ou uma constante do tipo `List`.

## Declaração e Atribuição

A declaração de uma variável ou constante List pode ser feito de forma duas formas

* **Explícita:** Deverá definir o tipo de variável explicitamente como List.

```csharp
List fruit = ['Apple', 'Orange', 'Banana']
```

* **Implícita:** Basta atribuir diretamente os valores a variável e o interpretador vai declara-lo implicitamente como `List<dynamic>`, sendo que os valores ficaram dentro dos colchetes e separados por vírgula.

```go
fruit := ['Apple', 'Orange', 'Banana']
```

Também é possível restringir o tipo de dados que a lista pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.\
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

```csharp
List<int> numbers = [1, 2, 3, 4, 5]

writeln numbers

# Output
> [1, 2, 3, 4, 5]
```

Existe a forma enxuta que é passando o **tipo dos valores** seguido de `[]`.

```csharp
int[] numbers = [1, 2, 3, 4, 5]

writeln numbers

# Output
> [1, 2, 3, 4, 5]
```

Também podemos utilizar uma matriz.

```csharp
int[] matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

writeln matrix[1][2]

# Output
> 6
```

## Referência de Valores

```csharp
int[] numbers = [1, 2, 3, 4, 5]

writeln numbers[1]

# Output
> 2
```

```csharp
int[] numbers = [1, 2, 3, 4, 5]

numbers[2] = 7

writeln numbers

# Output
> [1, 2, 7, 4, 5]
```

## Slice

Cria uma novo List baseado em partes de outro List.

```csharp
int[] numbers = [1, 2, 3, 4, 5]

writeln numbers[2:3]

# Output
> [3, 4]
```

```csharp
int[] numbers = [1, 2, 3, 4, 5]

writeln numbers[:]

# Output
> [1, 2, 3, 4, 5]
```

```csharp
int[] numbers = [1, 2, 3, 4, 5]

writeln numbers[:2]

# Output
> [1, 2, 3]
```

```csharp
int[] numbers = [1, 2, 3, 4, 5]

writeln numbers[2:]

# Output
> [3, 4, 5]
```

## Operações

```python
numbers := [1, 2, 3, 4, 5]

numbers = numbers + [6, 7, 8, 9, 10]
writeln numbers

# Output
> [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

```csharp
numbers := [1, 2, 3, 4, 5]

numbers = numbers - [2, 4]
writeln numbers

# Output
> [1, 3, 5]
```

```csharp
numbers := [1, 2, 3, 4, 5]

numbers = numbers * 2
writeln numbers

# Output
> [1, 2, 3, 4, 5, 1, 2, 3, 4, 5]
```

```csharp
numbers := [1, 2, 3, 4, 5]

writeln(5 in numbers)

# Output
> true
```

## Methods

Uma lista possui vários métodos úteis que podem ser utilizados.

### add

```csharp
int[] numbers = [1, 2, 3, 4, 5]
numbers.add(6)

writeln numbers

# Output
> [1, 2, 3, 4, 5, 6]
```

### insert

```csharp
int[] numbers = [1, 2, 3, 4, 5]
numbers.insert(6, 2)

writeln numbers

# Output
> [1, 2, 6, 3, 4, 5]
```

### remove

```csharp
int[] numbers = [1, 2, 3, 4, 5]
numbers.remove(2)

writeln numbers

# Output
> [1, 6, 3, 4, 5]
```

### pop

```csharp
int[] numbers = [1, 2, 3, 4, 5]
numbers.pop()

writeln numbers

# Output
> [1, 2, 6, 3, 4]
```

### reverse

```csharp
int[] numbers = [1, 2, 3, 4, 5]

writeln numbers.reverse

# Output
> [5, 4, 3, 2, 1]
```

### contains

```csharp
int[] numbers = [1, 2, 3, 4, 5]

writeln numbers.contains(1)
writeln numbers.contains(6)

# Output
> true
> false
```

### indexOf

```csharp
int[] numbers = [1, 2, 3, 4, 5]

writeln numbers.indexOf(1)

# Output
> 0
```

### sort

```csharp
int[] numbers = [4, 1, 5, 3, 2]

writeln numbers.sort

# Output
> [1, 2, 3, 4, 5]
```

### length

```csharp
int[] numbers = [1, 2, 3, 4, 5]

writeln numbers.length

# Output
> 5
```

### each

```csharp
int[] numbers = [1, 2, 3, 4, 5]

numbers.each(number -> writeln number)

# Output
> 1
> 2
> 3
> 4
> 5
```

### map

```csharp
int[] numbers = [1, 2, 3, 4, 5]

newNumbers := numbers.map(number -> number * 2)

writeln(newNumbers)

# Output
> [2, 4, 6, 8, 10]
```

### find

```csharp
int[] numbers = [1, 2, 3, 4, 5]

writeln numbers.find(3)

# Output
> 3
```

```dart
String[] colors = ['Red', 'Yellow', 'Blue', 'Orange', 'White']

writeln colors.find(r"[ed]")

# Output
> 'Red'
```

### findAll

```csharp
int[] numbers = [6, 2, 8, 3, 6]

writeln numbers.find(6)

# Output
> [6, 6]
```

```csharp
String[] colors = ['Red', 'Yellow', 'Blue', 'Orange', 'White']

writeln colors.find(r"[w]")

# Output
> ['Yellow', 'White']
```

### first

```csharp
String[] colors = ['Red', 'Yellow', 'Blue', 'Orange', 'White']

writeln colors.first()

# Output
> 'Red'
```

### last

```csharp
String[] colors = ['Red', 'Yellow', 'Blue', 'Orange', 'White']

writeln colors.last()

# Output
> 'White'
```

### sample

Pega aleatoriamente um item da lista.

```csharp
String[] colors = ['Red', 'Yellow', 'Blue', 'Orange', 'White']

writeln colors.sample()

# Output
> 'Yellow'
```

### max

```csharp
int[] numbers = [6, 2, 8, 3, 6]

writeln numbers.max()

# Output
> 8
```

### min

```csharp
int[] numbers = [6, 2, 8, 3, 6]

writeln numbers.min()

# Output
> 2
```

### sum

```csharp
int[] numbers = [6, 2, 8, 3, 6]

writeln numbers.sum()

# Output
> 25
```

### avg

```csharp
int[] numbers = [6, 2, 8, 3, 6]

writeln numbers.avg()

# Output
> 5
```
