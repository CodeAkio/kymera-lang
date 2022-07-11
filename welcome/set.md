---
description: É uma lista que não aceita itens repetidos.
---

# Tuple

## Introdução

O `Tuple` permite armazenar vários valores únicos de diferentes tipos que podem ser acessados através de um índice número que começa com o número 0.

Diferente de um List, o Tuple **não permite valores repetidos** e são **valores diferentes entre si**.

## Declaração e Atribuição

A declaração de uma variável ou constante Tuple pode ser feita de forma duas formas:

* **Explícita:** Deverá definir o tipo de variável explicitamente como Tuple.

```csharp
Tuple fruit = [:ok, 'Kym']
```

* **Implícita:** Basta atribuir diretamente os valores a variável dentro de `t[]` e o interpretador vai declara-lo implicitamente como `Tuple<dynamic>`, sendo que os valores ficaram dentro dos parênteses e separados por vírgula.

```go
var fruit = t['Apple', 'Orange', 'Banana']
```

Também é possível restringir o tipo de dados que o tuple pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.\
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

```
numbers = t<int>[1, 2, 3, 4, 5]

writeln(numbers)

# Output
> t[1, 2, 3, 4, 5]
```

Ou

```csharp
Tuple<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers)

# Output
> t[1, 2, 3, 4, 5]
```

## Uso Básico

Para acessar os valores, basta após o nome da variável usar **\[]** passando o **índice**.

Nesse caso estamos exibindo o valor armazenado em uma posição:

```csharp
Tuple<int> numbers = [1, 2, 3, 4, 5]

writeln(numers[0])

# Output
> 1
```

E neste estamos atualizando um valor em uma posição:

```csharp
Tuple<int> numbers = [1, 2, 3, 4, 5]

numers[1] = 8

writeln(numers)

# Output
> t[1, 8, 3, 4, 5]
```

## Methods

Um tuple possui vários métodos úteis que podem ser utilizados.

### add

```csharp
Tuple<int> numbers
numbers = [1, 2, 3, 4, 5]
numbers.add(6)

writeln(numbers)

# Output
> t[1, 2, 3, 4, 5, 6]
```

Veja o que ocorre ao tentar adicionar um valor duplicado:

```csharp
Tuple<int> numbers = [1, 2, 3, 4, 5]
numbers.add(6)
numbers.add(4)
numbers.add(1)

writeln(numbers)

# Output
> t[1, 2, 3, 4, 5, 6]
```

### insert

```csharp
Tuple<int> numbers = [1, 2, 3, 4, 5]
numbers.insert(6, 2)

writeln(numbers)

# Output
> t[1, 2, 6, 3, 4, 5]
```

### remove

```csharp
Tuple<int> numbers = [1, 2, 3, 4, 5]
numbers.remove(2)

writeln(numbers)

# Output
> t[1, 6, 3, 4, 5]
```

### pop

```csharp
Tuple<int> numbers = [1, 2, 3, 4, 5]
numbers.pop()

writeln(numbers)

# Output
> t[1, 2, 6, 3, 4]
```

### reverse

```csharp
Tuple<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.reverse())

# Output
> t[5, 4, 3, 2, 1]
```

### contains

```csharp
Tuple<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.contains(1))
writeln(numbers.contains(6))

# Output
> true
> false
```

### indexOf

```csharp
Tuple<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.indexOf(1))

# Output
> 0
```

### sort

```csharp
Tuple<int> numbers = [4, 1, 5, 3, 2]

writeln(numbers.sort())

# Output
> t[1, 2, 3, 4, 5]
```

### length

```csharp
Tuple<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.length)

# Output
> 5
```

### each

```csharp
Tuple<int> numbers = [1, 2, 3, 4, 5]

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
Tuple<int> numbers = [1, 2, 3, 4, 5]

var newNumbers = numbers.map(number => number * 2)

writeln(newNumbers)

# Output
> t[2, 4, 6, 8, 10]
```

### indexOf

```csharp
Tuple<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.indexOf(3))

# Output
> 2
```

### find

```csharp
Tuple<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.find(3))

# Output
> 3
```

```csharp
Tuple<string> colors = ['Red', 'Yellow', 'Blue', 'Orange', 'White']

writeln(colors.find(r"[ed]"))

# Output
> 'Red'
```

