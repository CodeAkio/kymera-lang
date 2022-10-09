---
description: Comandos de entrada pelo console
---

# Input Console

A classe Console possui vários métodos úteis para ler os dados informados pelo usuário.\
Estes métodos podem ser chamados sem precisar explicitar a classe Console, através de seus sugar syntax.

## read

O método Read serve para possibilitar a entrada de dados do usuário pelo teclado e retorna uma string do que foi digitado.

O método Read pode receber opcionalmente uma string como argumento. Esta string será mostrada no terminal antes da leitura de dados.

Opcionalmente pode passar o argumento type para dizer para qual tipo de dado o valor retornado deve ser parseado.

**Syntax:**

```go
read([text_to_print], type: <type_to_parse>)
```

**Exemplo:**

```go
var nome = read("Informe seu nome: ")
writeln("Seu nome é ${nome}.")

# Informe seu nome: Júlio
# Seu nome é Júlio.
```

### Parâmetros

Existem vários parâmetros utilizados pelo método read e readkey:

#### type

Ele faz o parsing da entrada para o tipo passado para ele.\
Caso informe um tipo de dado diferente do suportado, será retornado uma exceção do tipo TypeError.

```go
var name = read("What's your name?", type: string) // Jorge
var age = read("How old are you?", type: int) // 23
var gender = read("Are you man(M) or woman(W)?", type: char) // M

writeln(name)
writeln(age)
writeln(gender)

# "Jorge"
# 23
# 'M'
```

#### \<color>

É possível definir qual a cor da letra que será exibida na tela, para isso, basta passar o parâmetro nomeado 'color' e a cor.

## ReadOption

Em breve

## ReadOptions

Em breve

## ReadSlider

Em breve
