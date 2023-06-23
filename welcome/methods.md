# Functions

Uma função é definida pela keywork `fun`, com um identificador, seguido de parênteses abrindo e fechando **()** e utiliza a notação de pascal em sua declaração.

A definição do tipo de retorno é opcional, caso não informe nada, ele utilizará como padrão o tipo **void**.

**Syntax:**

```nim
fun <identificador>(<parâmetro> <tipo>) -> [tipo retorno] {
    <código>
}
```

**Exemplo:**

```nim
fun somarDoisNumeros(num1 float, num2 float) -> float {
    let soma = num1 + num2
    return soma
}

let valor_soma = somarDoisNumeros(10.0, 2.0)

writeln(valor_soma)

# 12.0
```



O `retorn` é opcional, basta definir o tipo de retorno e ele automaticamente retornará a última linha:

```nim
fun somarDoisNumeros(num1 folat, num2 float) -> float {
    num1 + num2
}

let valor_soma = somarDoisNumeros(10.0, 2.0)

writeln(valor_soma)

# 12.0
```



Quando os parâmetros são do mesmo tipo, basta apenas informar no último:

```nim
fun somarDoisNumeros(num1, num2 float) -> float {
    num1 + num2
}

var valor_soma = somarDoisNumeros(10.0, 2.0)

writeln(valor_soma)

# 12.0
```



Também é possível ter **múltiplos retornos**:

```kotlin
fun swap(num1, num2 int) -> (int, int) {
    return num2, num1
}
```

```kotlin
fun swap(num1, num2 int) -> (int, int) | null {
    # Some code
}
```



Podemos trabalhar com sobre carga que funciona em cima de **pattern matching**.

```kotlin
fun log(%[:error, message string]) {
    writeln("Something went wrong: ${message}")
}

fun log(%[:ok, message string]) {
    writeln("It works: ${message}")
}
```



As funções podem ter cláusula de guarda, que são decorators que definem uma condição para a função ser executada:

```kotlin
@when(idade >= 18)
fun verificaIdade(idade int) {
    writeln("Maior de idade")
}

@when(idade < 18)
fun verificaIdade(idade int) {
    writeln("Menor de idade")
}
```



Podemos trabalhar com funções anônimas, criando funções sem identificadores:

```typescript
(num1, num2 float) -> float {
    num1 + num2
}
```



Para fazer o **in line**, basta usar o _arrow function_ e o tipo de retorno se torna implícito:

```typescript
(num1, num2 float) => num1 + num2
```

```kotlin
(name string) => "Hello ${name}"
```



Podemos usar o receiver que é um argumento que recebemos antes do nome da função, ele tem um comportamento similar ao de um método de POO, mas ele é mais flexível:

```kotlin
fun (p Person) andar() {
    writeln("Andando...")
}

let p = Person()
p.andar()
```

```kotlin
fun (*i ItemPedido) adicionar(quantidade int) {
    i.quantidade += quantidade
}

let item = ItemPedido(nome: "Tênis", quantidade: 1)
item.adicionar(2) // 3
```
