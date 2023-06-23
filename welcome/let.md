# Let

O let é parecido com var, mas é de **atribuição única**, após a primeira atribuição, o valor não pode ser alterado.

Diferente da constante, ele é processado em **tempo de execução** e permite postergar a atribuição.

**Sintaxe:**

```go
# With type definition
<variable_name> <type> = <value>

# With type inference
let <variable_name> = <value>

# Assignment value after declaration
<variable_name> = <value>
```

**Exemplo:**

```nim
let number int
number = 10
writeln(number)
# 10

let animal = "Dog"
writeln(animal)
# "Dog"

animal = "Cat"
# Error!
```
