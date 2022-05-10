# Functions

Uma função é definida com um identificador seguido de parênteses abrindo e fechando **()** e utiliza a notação de pascal em sua declaração.

A definição do tipo de retorno é opcional, caso não informe nada, ele utilizará como padrão o tipo **void**.

**Syntax:**

```kotlin
fun <identificador>([tipo] <parâmetro>) -> [tipo retorno] {
    <código>
}
```

**Exemplo:**

```kotlin
fun somarDoisNumeros(folat num1, float num2) -> float {
    soma := num1 + num2
    return soma
}

valor_soma := somarDoisNumeros(10.0, 2.0)

writeln valor_soma

# Output
> 12.0
```

O retorno é opcional, basta definir o tipo de retorno e ele automaticamente retornará a última linha:

```kotlin
fun somarDoisNumeros(folat num1, float num2) -> float {
    num1 + num2kot
}

valor_soma := somarDoisNumeros(10.0, 2.0)

writeln valor_soma

# Output
> 12.0
```

Também é possível ter múltiplos retornos:

```kotlin
fun swap(int num1, int num2) -> (int, int) {
    return num2, num1
}
```

```kotlin
fun swap(int num1, int num2) -> (int, int) | null {
    pass
}
```

Podemos trabalhar com sobre carga que funciona em cima de pattern matching.

```kotlin
fun log(%[ :error, string message ]) {
    writeln 'Something went wrong: ${message}'
}

fun log(%[ :ok, string message ]) {
    writeln 'It works: ${message}'
}
```

As funções podem ter clausula de guarda, que são decorators que definem uma condição para a função ser executada:

```kotlin
@when(idade >= 18)
fun verificaIdade(int idade) {
    writeln 'Maior de idade'
}

@when(idade < 18)
fun verificaIdade(int idade) {
    writeln 'Menor de idade'
}
```

Podemos trabalhar com funções anônimas:

```typescript
fn(float num1, float num2) -> float {
    num1 + num2
}
```

```typescript
fn(float num1, float num2) -> float, do: num1 + num2
```

```kotlin
fn(string name) -> string, do: 'Hello ${name}'
```
