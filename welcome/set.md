---
description: É uma lista que não aceita itens repetidos.
---

# Tuple

## Introdução

O `Set` permite armazenar vários valores únicos de diferentes tipos que podem ser acessados através de um índice número que começa com o número 0.

Diferente de um List, o Set **não permite valores repetidos** e são **valores diferentes entre si**.

## Declaração e Atribuição

A declaração de uma variável ou constante Set pode ser feita de forma duas formas:

* **Explícita:** Deverá definir o tipo de variável explicitamente como Set.

```csharp
Set fruit = t{'Apple', 'Orange', 'Banana'}
```

* **Implícita:** Basta atribuir diretamente os valores a variável e o interpretador vai declara-lo implicitamente como `Set<dynamic>`, sendo que os valores ficaram dentro dos parênteses e separados por vírgula.

```go
fruit := ('Apple', 'Orange', 'Banana')
```

Também é possível restringir o tipo de dados que o set pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.\
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

```csharp
Set<int> numbers = (1, 2, 3, 4, 5)

writeln(numbers)

# Output
> (1, 2, 3, 4, 5)
```

## Uso Básico

Para acessar os valores, basta após o nome da variável usar **\[]** passando o **índice**.

Nesse caso estamos exibindo o valor armazenado em uma posição:

```csharp
Set<int> numbers = (1, 2, 3, 4, 5)

writeln(numers[0])

# Output
> 1
```

E neste estamos atualizando um valor em uma posição:

```csharp
Set<int> numbers = (1, 2, 3, 4, 5)

numers[1] = 8

writeln(numers)

# Output
> (1, 8, 3, 4, 5)
```

## Methods

Um set possui vários métodos úteis que podem ser utilizados.

### add

```csharp
Set<int> numbers
numbers = (1, 2, 3, 4, 5)
numbers.add(6)

writeln(numbers)

# Output
> (1, 2, 3, 4, 5, 6)
```

Veja o que ocorre ao tentar adicionar um valor duplicado:

```csharp
Set<int> numbers = (1, 2, 3, 4, 5)
numbers.add(6)
numbers.add(4)
numbers.add(1)

writeln(numbers)

# Output
> (1, 2, 3, 4, 5, 6)
```

### insert

```csharp
Set<int> numbers = (1, 2, 3, 4, 5)
numbers.insert(6, 2)

writeln(numbers)

# Output
> (1, 2, 6, 3, 4, 5)
```

### remove

```csharp
Set<int> numbers = (1, 2, 3, 4, 5)
numbers.remove(2)

writeln(numbers)

# Output
> (1, 6, 3, 4, 5)
```

### pop

```csharp
Set<int> numbers = (1, 2, 3, 4, 5)
numbers.pop()

writeln(numbers)

# Output
> (1, 2, 6, 3, 4)
```

### reverse

```csharp
Set<int> numbers = (1, 2, 3, 4, 5)

writeln(numbers.reverse)

# Output
> (5, 4, 3, 2, 1)
```

### contains

```csharp
Set<int> numbers = (1, 2, 3, 4, 5)

writeln(numbers.contains(1))
writeln(numbers.contains(6))

# Output
> true
> false
```

### indexOf

```csharp
Set<int> numbers = (1, 2, 3, 4, 5)

writeln(numbers.indexOf(1))

# Output
> 0
```

### sort

```csharp
Set<int> numbers = (4, 1, 5, 3, 2)

writeln(numbers.sort)

# Output
> [1, 2, 3, 4, 5]
```

### length

```csharp
Set<int> numbers = (1, 2, 3, 4, 5)

writeln(numbers.length)

# Output
> 5
```

### each

```csharp
Set<int> numbers = (1, 2, 3, 4, 5)

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
Set<int> numbers = (1, 2, 3, 4, 5)

newNumbers := numbers.map(number => number * 2)

writeln(newNumbers)

# Output
> (2, 4, 6, 8, 10)
```

### indexOf

```csharp
Set<int> numbers = (1, 2, 3, 4, 5)

writeln(numbers.indexOf(3))

# Output
> 2
```

### find

```csharp
Set<int> numbers = (1, 2, 3, 4, 5)

writeln(numbers.find(3))

# Output
> 3
```

```csharp
Set<string> colors = ('Red', 'Yellow', 'Blue', 'Orange', 'White')

writeln(colors.find(r"[ed]"))

# Output
> 'Red'
```

