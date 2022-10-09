---
description: >-
  É uma estrutura de chave valor, conhecido em outras linguagens como Hash ou
  Dict.
---

# Map

## Introdução

O `Map` permite armazenar dados na estrutura de chave e valor.

Ele não permite que haja chaves duplicadas.

Caso queira ter mais controle de chaves pré-definidas e os tipos dos valores, deverá usar um _Struct_.

## Declaração e Atribuição

A declaração de uma variável ou constante Map pode ser feita de forma duas formas:

* **Explícita:** Deverá definir o tipo de variável explicitamente como `Map`.

```csharp
Map user = {
    name: "Pedro",
    age: 22
}
```

* **Implícita:** Basta atribuir diretamente as chaves e valores a variável e o interpretador vai declara-lo implicitamente como `Map<atom, dynamic>`, sendo que as chaves e valores ficaram dentro de chaves e separados por vírgula.

```go
var user = {
    name: "Pedro",
    age: 22
}
```

Também é possível restringir o tipo de dados que o Map pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.\
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

```csharp
Map<string, string> numbers = {
    "name": "Pedro",
    "age": "22"
}

writeln(numbers)

# {
    "name": "Pedro",
    "age": "22"
}
```

## Methods

Um Map possui vários métodos úteis que podem ser utilizados.

### add

```csharp
var user = {
    name: "Pedro",
    age: 22
}

user.add(:email, "pedro@email.com")

writeln(user)

# {
    name: "Pedro",
    age: 22,
    email: "pedro@email.com"
}
```

Ao tentar adicionar uma chave duplicada, ele chama o **update**:

```csharp
var user = {
    name: "Pedro",
    age: 22
}

user.add(:name, "Marcos")

writeln(user)

# {
    name: "Marcos",
    age: 22
}
```

### update

```kotlin
var user = {
    name: "Pedro",
    age: 22
}

user.update(:name, "Marcos")

writeln(user)

# {
    name: "Marcos",
    age: 22
}
```

### remove

```csharp
var user = {
    name: "Pedro",
    age: 22
}

user.remove(:age)

writeln(user)

# {
    name: "Pedro"
}
```

### keys

```csharp
var user = {
    name: "Pedro",
    age: 22
}

writeln(user.values)

# [:name, :age]
```

### values

```kotlin
var user = {
    name: "Pedro",
    age: 22
}

writeln(user.values)

# Output
> ["Pedro", 22]
```

### any

```kotlin
var user = {
    name: "Pedro",
    age: 22
}

writeln(user.has(:age, 22))

# Output
> true
```

```csharp
var user = {
    name: "Pedro",
    age: 22
}

writeln(user.has(:age, 23))

# Output
> false
```

### hasKey

```csharp
var user = {
    name: "Pedro",
    age: 22
}

writeln(user.hasKey(:age))

# Output
> true
```

### hasValue

```kotlin
var user = {
    name: "Pedro",
    age: 22
}

writeln(user.hasValue("Pedro"))

# Output
> t[:name]
```

[https://ruby-doc.org/core-3.0.2/Hash.html](https://ruby-doc.org/core-3.0.2/Hash.html)

