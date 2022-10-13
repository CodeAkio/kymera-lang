# Tuple \[WIP]



## Introdução

O `Tuple` é uma lista imutável de valores de tipos variados, geralmente cada uma das duas posições representa um valor.

{% hint style="info" %}
Ele deve ser usado apenas para pequenas quantidade de dados, mais de 3 valores é indicado o uso de um Map ou Classe.
{% endhint %}

## Declaração e Atribuição

A declaração de uma variável ou constante Tuple pode ser feito de forma duas formas

* **Explícita:** Deverá definir o tipo de variável explicitamente como Tuple.

```swift
conn Tuple = t[200, "Ok"]
```

* **Implícita:** Basta atribuir diretamente os valores a variável e o interpretador vai declará-lo implicitamente como `Tuple<dyn>`, sendo que os valores ficaram dentro de `t[]` e separados por vírgula.

```go
var conn = t[200, "Ok"]
```



Também é possível restringir o tipo de dados que a tupla pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.\
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

```swift
conn Tuple<int, string> = [200, "Ok"]

writeln(conn)

# t[200, "Ok"]
```

## Referência de Valores

```csharp
conn = t[200, "Ok"]

writeln(conn[1])

# Ok
```

```csharp
error = t[2332, "An unknown error"]

error[1] = "A connection error"

writeln(error)

# t[2332, "A connection error"]
```



## Methods

Uma lista possui vários métodos úteis que podem ser utilizados.

### contains

```csharp
numbers = t[1, 2, 3, 4, 5]

writeln(numbers.contains(1))
writeln(numbers.contains(6))

# true
# false
```

### indexOf

```csharp
numbers int[] = [1, 2, 3, 4, 5]

writeln(numbers.indexOf(1))

# 0
```

### length

```csharp
numbers int[] = [1, 2, 3, 4, 5]

writeln(numbers.length())

# 5
```

### each

```csharp
numbers int[] = [1, 2, 3, 4, 5]

numbers.each(number => writeln(number))

# 1
# 2
# 3
# 4
# 5
```

### map

```csharp
numbers int[] = [1, 2, 3, 4, 5]

var newNumbers = numbers.map(number => number * 2)

writeln(newNumbers)

# [2, 4, 6, 8, 10]
```

### find

```csharp
numbers int[] = [1, 2, 3, 4, 5]

writeln(numbers.find(3))

# 3
```

```csharp
colors string[] = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.find(r"[ed]"))

# "Red"
```

### first

```csharp
colors string[] = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.first())

# "Red"
```

### last

```csharp
colors string[] = ["Red", "Yellow", "Blue", "Orange", "White"]

writeln(colors.last())

# "White"
```
