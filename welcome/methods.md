# Functions

Uma função é definida com um identificador seguido de parenteses abrindo e fechando **\(\)** e utiliza a notação de pascal em sua declaração.

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
    resultado := num1 + num2
    return resultado
}

valor_soma := somarDoisNumeros(10.0, 2.0)

write(valor_soma)

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
fun swap(int num1, int num2) -> (int, int) | Error {
    return num2, num1
}
```

Podemos trabalhar com sobre carga que funciona em cima de pattern matching.

```kotlin
fun log(%[:error, string message]) {
    write('Something went wrong: ${message}')
}

fun log(%[:ok, string message]) {
    write('It works: ${message}')
}
```

As funções podem ter clausula de guarda, que são decorators que definem uma condição para a função ser executada:

```kotlin
@when(idade >= 18)
fun verificaIdade(int idade) {
    write('Maior de idade')
}

@when(idade < 18)
fun verificaIdade(int idade) {
    write('Menor de idade')
}
```

