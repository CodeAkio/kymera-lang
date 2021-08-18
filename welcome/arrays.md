---
description: Como utilizar a interface IList
---

# List

## Introdução

O List permite armazenar vários valores de diferentes tipos que podem ser acessados através de um índice número que começa com o número 0. Esses múltiplos valores são armazenados em uma variável ou uma constante do tipo List.

## Declaração e Atribuição

A declaração de uma variável ou constante List pode ser feito de forma duas formas

* **Explícita:** Deverá definir o tipo de variável explicitamente como List.

```csharp
List fruit = ['Apple', 'Orange', 'Banana']
```

* **Implícita:** Basta atribuir diretamente os valores a variável e o interpretador vai declara-lo implicitamente como _List&lt;dynamic&gt;_, sendo que os valores ficaram dentro dos colchetes e separados por vírgula.

```go
fruit := ['Apple', 'Orange', 'Banana']
```

Também é possível restringir o tipo de dados que a lista pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.  
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

```csharp
List<int> numbers = [1, 2, 3, 4, 5]

write(numbers)

# Output
> [1, 2, 3, 4, 5]
```

## Methods

Uma lista possui vários métodos úteis que podem ser utilizados.

### add

```csharp
List<int> numbers = [1, 2, 3, 4, 5]
numbers.add(6)

write(numbers)

# Output
> [1, 2, 3, 4, 5, 6]
```

### insert

```csharp
List<int> numbers = [1, 2, 3, 4, 5]
numbers.insert(6, 2)

write(numbers)

# Output
> [1, 2, 6, 3, 4, 5]
```

### remove

```csharp
List<int> numbers = [1, 2, 3, 4, 5]
numbers.remove(2)

write(numbers)

# Output
> [1, 6, 3, 4, 5]
```

### pop

```csharp
List<int> numbers = [1, 2, 3, 4, 5]
numbers.pop()

write(numbers)

# Output
> [1, 2, 6, 3, 4]
```

### reverse

```csharp
List<int> numbers = [1, 2, 3, 4, 5]

write(numbers.reverse)

# Output
> [5, 4, 3, 2, 1]
```

### contains

```csharp
List<int> numbers = [1, 2, 3, 4, 5]

write(numbers.contains(1))
write(numbers.contains(6))

# Output
> true
> false
```

### indexOf

```csharp
List<int> numbers = [1, 2, 3, 4, 5]

write(numbers.indexOf(1))

# Output
> 0
```

### sort

```csharp
List<int> numbers = [4, 1, 5, 3, 2]

write(numbers.sort)

# Output
> [1, 2, 3, 4, 5]
```

### count

```csharp
List<int> numbers = [1, 2, 3, 4, 5]

write(numbers.count)

# Output
> 5
```





