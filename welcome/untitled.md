---
description: Comandos para gerar saída pelo console
---

# Output Console

A classe Console possui vários métodos úteis para imprimir dados na tela.  
Estes métodos podem ser chamados sem precisar explicitar a classe Console, através de seus sugar syntax.

**Exemplo:**

```text
Console.write() #Forma explicita
write() #sugar syntax de Console.write()
```

Recomenda-se que utilize o sugar syntax por ser menos verboso e natural para ler.

## Console.write

Este método imprime uma mensagem passada como argumento na tela sem pular linha.

**Syntax:**

```text
Console.write(<mensagem>)
# OR
write(<mensagem>)
```

**Exemplo:**

```text
nome = "Marcos"
write("Meu nome é ")
write(nome)

# Output
> "Meu nome é Marcos"
```

## Console.writeLn

Este método imprime uma mensagem passada como argumento na tela e ao final quebra a linha.

**Syntax:**

```text
Console.WriteLn(<mensagem>)
# OR
writeLn(<mensagem>)
```

