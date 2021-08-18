# Lambda

As operações lambda podem ser feitas em qualquer coleção de dados que implementa **IEnumerable** \(List, Set e String\) e também pode se aplicar ao **Dict**.

### map

Percorre todos os elementos realiza alguma operação e retorna uma nova coleção.

```csharp
name := "Kym"

newName := name.map(letter => letter + ".")

writeln(newName)

# Output
> "K.y.m."
```

```csharp
List<int> numbers = [1, 2, 3, 4, 5]

newNumbers := numbers.map(number => number * 2)

writeln(newNumbers)

# Output
> [2, 4, 6, 8, 10]
```

```csharp
Set<int> numbers = (1, 2, 3, 4, 5)

newNumbers := numbers.map(number => number * 2)

writeln(newNumbers)

# Output
> (2, 4, 6, 8, 10)
```

```csharp
user := {
    name: "Pedro",
    age: 22
}

user.map((key, value) => [key, isString(name) ? value.toUpper() : value])

# Output
> user := {
    name: "PEDRO",
    age: 22
}
```

