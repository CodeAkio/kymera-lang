# Functions

Uma função é definida com um identificador seguido de parenteses abrindo e fechando **\(\)** e utiliza a notação de pascal em sua declaração.

A definição do tipo de retorno é opcional, caso não informe nada, ele utilizará como padrão o tipo **void**.

**Syntax:**

```text
fun <identificador> ([tipo] <parâmetro>) -> [tipo retorno] {
    <código>
}
```

**Exemplo:**

```text
fun somarDoisNumeros (float num1, float num2) -> float {
    resultado = num1 + num2
    return resultado
}

valor_soma = somarDoisNumeros(10.0, 2.0)

write(valor_soma)

# Output
> 12.0
```

