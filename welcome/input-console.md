---
description: Comandos de entrada pelo console
---

# Input Console

A classe Console possui vários métodos úteis para ler os dados informados pelo usuário.\
Estes métodos podem ser chamados sem precisar explicitar a classe Console, através de seus sugar syntax.

## readln

O método `readln` lê a entrada de dados do usuário pelo teclado e retorna uma string do que foi digitado.

Ele lê apenas a linha, então ele armazena tudo que o usuário digitou até apertar a tecla **Enter**.

Ele recebe opcionalmente uma string como argumento, que será mostrada no terminal antes da leitura de dados.

Opcionalmente pode passar o argumento `type` para fazer o parsing dos dados.

**Syntax:**

```go
readln([text_to_print], type: <type_to_parse>)
```

**Exemplo:**

```nim
let nome = readln("Informe seu nome: ")
writeln("Seu nome é ${nome}.")

# Informe seu nome: Júlio
# Seu nome é Júlio.
```

### Parâmetros

#### type

Ele faz o parsing da entrada para o tipo passado para ele.\
Caso informe um tipo de dado diferente do suportado, será retornado uma exceção do tipo TypeError.

```nim
let name = read("What's your name?", type: string) # Jorge
let age = read("How old are you?", type: int) # 23
let gender = read("Are you man(M) or woman(W)?", type: char) # M

writeln(name)
writeln(age)
writeln(gender)

# "Jorge"
# 23
# c"M"
```

#### \<color>

É possível definir qual a cor da letra que será exibida na tela, para isso, basta passar o parâmetro nomeado 'color' e a cor.

## Read

Ele é similar ao readln, porém lê  múltiplas linhas e para enviar os dados deve usar as teclas **CTRL + Enter**.

```nim
let text = readkey("Write your comment:")
writeln(text)

# It's a very long text
# It has a lot of lines
```

## ReadKey

Ele é similar ao readln, porém lê apenas 1 caractere e não precisa teclar **Enter**.

```nim
let gender = readkey("What is your gender? (m/f)")
writeln(gender)

# m
```

## ReadOption

Em breve

## ReadOptions

Em breve

## ReadSlider

Em breve
