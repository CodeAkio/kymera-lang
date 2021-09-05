---
description: Comandos para gerar saída pelo console
---

# Output Console

A classe Console possui vários métodos úteis para imprimir dados na tela.  
Estes métodos podem ser chamados sem precisar explicitar a classe Console, através de seus sugar syntax.

## write

Este método imprime uma mensagem passada como argumento na tela sem pular linha.

**Syntax:**

```go
write(<mensagem>)
```

**Exemplo:**

```go
nome := 'Marcos'
write('Meu nome é ')
write(nome)

# Output
> Meu nome é Marcos
```

## writeln

Este método imprime uma mensagem passada como argumento na tela e ao final quebra a linha.

**Syntax:**

```go
writeln(<mensagem>)
```

**Exemplo:**

```go
nome := 'Marcos'
writeln('Meu nome é ')
writeln(nome)

# Output
> Meu nome é 
> Marcos
```

