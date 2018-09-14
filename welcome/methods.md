# Functions

Uma função é definida com a palavra reservada **func** e utiliza a notação de pascal em sua declaração.

A definição do retorno é opcional, caso não informe nada, ele será declarado como **void**.

**Syntax:**

```text
func <identificado>(<parâmetro>: [tipo]): <tipo retorno> {
    <código>
}
```

**Exemplo¹:**

```text
func somarDoisNumeros(num1: float, num2: float): float {
    resultado = num1 + num2
    return resultado
}

valor_soma = somarDoisNumeros(10.0, 2.0)

write(valor_soma)

# Output
> 12.0
```

