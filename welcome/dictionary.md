---
description: >-
  É uma estrutura de chave valor, conhecido em outras linguagens como Hash ou
  Map.
---

# Dict

## Introdução

O `Dict` permite armazenar dados na estrutura de chave e valor.

Ele não permite que haja chaves duplicadas.

Caso queira ter mais controle de chaves pré-definidas e os tipos dos valores, deverá usar um _Struct_.

## Declaração e Atribuição

A declaração de uma variável ou constante Dict pode ser feita de forma duas formas:

* **Explícita:** Deverá definir o tipo de variável explicitamente como `Dict`.

```csharp
Dict user = {
    name: 'Pedro',
    age: 22
}
```

* **Implícita:** Basta atribuir diretamente as chaves e valores a variável e o interpretador vai declara-lo implicitamente como `Dict<atom, dynamic>`, sendo que as chaves e valores ficaram dentro de chaves e separados por vírgula.

```go
var user = {
    name: 'Pedro',
    age: 22
}
```

Também é possível restringir o tipo de dados que o Dict pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.\
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

```csharp
Dict<string, string> numbers = {
    'name': 'Pedro',
    'age': '22'
}

writeln numbers

# Output
> {
    'name': 'Pedro',
    'age': '22'
}
```

## Methods

Um Dict possui vários métodos úteis que podem ser utilizados.

### add

```csharp
var user = {
    name: 'Pedro',
    age: 22
}

user.add(:email, 'pedro@email.com')

writeln user

# Output
> {
    name: 'Pedro',
    age: 22,
    email: 'pedro@email.com'
}
```

Ao tentar adicionar uma chave duplicada, ele chama o **update**:

```csharp
var user = {
    name: 'Pedro',
    age: 22
}

user.add(:name, 'Marcos')

writeln user

# Output
> {
    name: 'Marcos',
    age: 22
}
```

### update

```python
var user = {
    name: 'Pedro',
    age: 22
}

user.update(:name, 'Marcos')

writeln user

# Output
> {
    name: 'Marcos',
    age: 22
}
```

### remove

```csharp
var user = {
    name: 'Pedro',
    age: 22
}

user.remove(:age)

writeln user

# Output
> {
    name: 'Marcos'
}
```

### keys

```ruby
var user = {
    name: 'Pedro',
    age: 22
}

writeln user.values

# Output
> [:name, :age]
```

### values

```ruby
var user = {
    name: 'Pedro',
    age: 22
}

writeln user.values

# Output
> ['Pedro', 22]
```

### any

```ruby
var user = {
    name: 'Pedro',
    age: 22
}

writeln user.has(:age, 22)

# Output
> true
```

```csharp
var user = {
    name: 'Pedro',
    age: 22
}

writeln user.has?(:age, 23)

# Output
> false
```

### hasKey

```csharp
var user = {
    name: 'Pedro',
    age: 22
}

writeln user.hasKey?(:age)

# Output
> true
```

### hasValue

```ruby
var user = {
    name: 'Pedro',
    age: 22
}

writeln user.hasValue('Pedro')

# Output
> t[:name]
```

[https://ruby-doc.org/core-3.0.2/Hash.html](https://ruby-doc.org/core-3.0.2/Hash.html)

