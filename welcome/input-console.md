---
description: Comandos de entrada pelo console
---

# Input Console

A classe Console possui vários métodos úteis para ler os dados informados pelo usuário.  
Estes métodos podem ser chamados sem precisar explicitar a classe Console, através de seus sugar syntax.

## read

O método Read serve para possibilitar a entrada de dados do usuário pelo teclado e retorna uma string do que foi digitado.

O método Read pode receber opcionalmente uma string como argumento. Esta string será mostrada no terminal antes da leitura de dados.

**Syntax:**

```go
read([text to print])
```

**Exemplo:**

```go
nome := read("Informe seu nome: ")
write("Seu nome é ${nome}.")

# Output
# Foi digitado 'Júlio' no terminal
> Informe seu nome: Júlio
> Seu nome é Júlio.
```

### Parâmetros

Existem vários parâmetros utilizados pelo método read e readkey:

#### &lt;type&gt;

É possível definir qual o tipo de dado é aceito como entrada passando o tipo no generic.  
Definido um tipo além de restringir o tipo de dado a ser aceito como entrada, o método read em vez de retornar uma string, ele retornará o valor recebido com o tipo de dado definido, ou seja, se definir o tipo como inteiro, ele só aceita números inteiros e retorna inteiros.  
Caso informe um tipo de dado diferente do suportado, será retornado uma exceção do tipo TypeError.

```go
name := read(String, "What's your name?") // Jorge
age := read(int, 'How old are you?') // 23
gender := read(char, 'Are you man(M) or woman(W)?') // M

write(name)
write(age)
write(gender)

# Output
> "Jorge"
> 23
> 'M'
```

#### &lt;color&gt;

É possível definir qual a cor da letra que será exibida na tela, para isso, basta passar o parâmetro nomeado 'color' e a cor.

## ReadOption

Em breve

## ReadOptions

Em breve

## ReadSlider

Em breve

