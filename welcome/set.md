---
description: É uma lista que não aceita itens repetidos.
---

# Set

## Introdução

O `Set` permite armazenar vários valores únicos de diferentes tipos que podem ser acessados através de um índice número que começa com o número 0.

Diferente de um List, o Set **não permite valores repetidos** e são **valores diferentes entre si**.

## Declaração e Atribuição

A declaração de uma variável ou constante Set pode ser feita de forma duas formas:

* **Explícita:** Deverá definir o tipo de variável explicitamente como Set.

```csharp
Set fruit = [:ok, "Kym"]
```

* **Implícita:** Basta atribuir diretamente os valores a variável dentro de `set[]` e o interpretador vai declara-lo implicitamente como `Set<dynamic>`, sendo que os valores ficaram dentro dos parênteses e separados por vírgula.

```go
var fruit = set["Apple", "Orange", "Banana"]
```

Também é possível restringir o tipo de dados que o set pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.\
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

<pre class="language-csharp"><code class="lang-csharp"><strong>var numbers = set&#x3C;int>[1, 2, 3, 4, 5]
</strong>
writeln(numbers)

# set[1, 2, 3, 4, 5]</code></pre>

Ou

```csharp
Set<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers)

# set[1, 2, 3, 4, 5]
```

## Uso Básico

Para acessar os valores, basta após o nome da variável usar **\[]** passando o **índice**.

Nesse caso estamos exibindo o valor armazenado em uma posição:

```csharp
Set<int> numbers = [1, 2, 3, 4, 5]

writeln(numers[0])

# Output
> 1
```

E neste estamos atualizando um valor em uma posição:

```csharp
Set<int> numbers = [1, 2, 3, 4, 5]

numers[1] = 8

writeln(numers)

# set[1, 8, 3, 4, 5]
```

## Methods

Um set possui vários métodos úteis que podem ser utilizados.

### add

```csharp
Set<int> numbers
numbers = [1, 2, 3, 4, 5]
numbers.add(6)

writeln(numbers)

# set[1, 2, 3, 4, 5, 6]
```

Veja o que ocorre ao tentar adicionar um valor duplicado:

```csharp
Set<int> numbers = [1, 2, 3, 4, 5]
numbers.add(6)
numbers.add(4)
numbers.add(1)

writeln(numbers)

# set[1, 2, 3, 4, 5, 6]
```

### insert

```csharp
Set<int> numbers = [1, 2, 3, 4, 5]
numbers.insert(6, 2)

writeln(numbers)

# set[1, 2, 6, 3, 4, 5]
```

### remove

```csharp
Set<int> numbers = [1, 2, 3, 4, 5]
numbers.remove(2)

writeln(numbers)

# set[1, 6, 3, 4, 5]
```

### pop

```csharp
Set<int> numbers = [1, 2, 3, 4, 5]
numbers.pop()

writeln(numbers)

# set[1, 2, 6, 3, 4]
```

### reverse

```csharp
Set<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.reverse())

# set[5, 4, 3, 2, 1]
```

### contains

```csharp
Set<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.contains(1))
writeln(numbers.contains(6))

# true
# false
```

### indexOf

```csharp
Set<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.indexOf(1))

# 0
```

### sort

```csharp
Set<int> numbers = [4, 1, 5, 3, 2]

writeln(numbers.sort())

# set[1, 2, 3, 4, 5]
```

### length

```csharp
Set<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.length)

# 5
```

### each

```csharp
Set<int> numbers = [1, 2, 3, 4, 5]

numbers.each(number => writeln(number))

# 1
# 2
# 3
# 4
# 5
```

### map

```csharp
Set<int> numbers = [1, 2, 3, 4, 5]

var newNumbers = numbers.map(number => number * 2)

writeln(newNumbers)

# set[2, 4, 6, 8, 10]
```

### indexOf

```csharp
Set<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.indexOf(3))

# 2
```

### find

```csharp
Set<int> numbers = [1, 2, 3, 4, 5]

writeln(numbers.find(3))

# 3
```

```csharp
Set<string> colors = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.find(r"[ed]"))

# "Red"
```

