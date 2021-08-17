# Functions

Uma função é definida com um identificador seguido de parenteses abrindo e fechando **\(\)** e utiliza a notação de pascal em sua declaração.

A definição do tipo de retorno é opcional, caso não informe nada, ele utilizará como padrão o tipo **void**.

**Syntax:**

```text
fun <identificador> (<parâmetro> [tipo]) [tipo retorno] {
    <código>
}
```

**Exemplo:**

```text
fun somarDoisNumeros (num1 folat, num2 float) float {
    resultado = num1 + num2
    return resultado
}

valor_soma := somarDoisNumeros(10.0, 2.0)

write(valor_soma)

# Output
> 12.0
```

Também é possível ter múltiplos retornos:

```text
fun swap (num1 int, num2 int) (int, int) {
    return num2, num1
}
```

Podemos trabalhar com sobre carga que funciona em cima de pattern matching.

```text
fun log (%[:error, message String]) {
    write("Something went wrong: ${message}")
}

fun log (%[:ok, message String]) {
    write("It works: ${message}")
}
```

As funções podem ter clausula de guarda, que são decorators que definem uma condição para a função ser executada:

```text
@when(idade >= 18)
fun verificaIdade (idade int) {
    write('Maior de idade')
}

@when(idade < 18)
fun verificaIdade (idade int) {
    write('Menor de idade')
}
```

