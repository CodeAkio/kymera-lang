# Tuple



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

### length

```csharp
user = t[22, "Pedro", 2000.00]

writeln(user.length())

# 3
```

### each

```csharp
user = t[22, "Pedro", 2000.00]

user.each(data => writeln(data))

# 22
# Pedro
# 2000.00
```

### map

```csharp
user = t[22, "Pedro", 2000.00]

var newUser = user.map(data => if data is string then data.toUpper() else data)

writeln(newUser)

# t[22, "PEDRO", 2000.00]
```

### find

```csharp
user = t[22, "Pedro", 2000.00]

writeln(user.find(22))

# 22
```

```csharp
user = t[22, "Pedro", 2000.00]

writeln(user.find(r"[dro]"))

# "Pedro"
```

### findAll

```csharp
user = t[22, "Pedro", 2000.00]

writeln(user.findAll(22))

# [22]
```

```csharp
user = t[22, "Pedro", 2000.00]

writeln(user.findAll(r"[dro]"))

# ["Pedro"]
```

### first

```csharp
user = t[22, "Pedro", 2000.00]

writeln(user.first())

# 22
```

### last

```csharp
user = t[22, "Pedro", 2000.00]

writeln(user.last())

# 2000.00
```
