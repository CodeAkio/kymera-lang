---
description: Comandos de entrada pelo console
---

# Input Console

A classe Console possui vários métodos úteis para ler os dados informados pelo usuário.  
Estes métodos podem ser chamados sem precisar explicitar a classe Console, através de seus sugar syntax.

**Exemplo:**

```text
Console.Read() #Forma explicita
read() #sugar syntax de Console.Read()
```

Recomenda-se que utilize o sugar syntax por ser menos verboso e natural para ler.

## Console.Read

O método Read serve para possibilitar a entrada de dados do usuário pelo teclado e retorna uma string do que foi digitado.

O método Read pode receber opcionalmente uma string como argumento. Esta string será mostrada no terminal antes da leitura de dados.

**Syntax:**

```text
Console.Read(<user input>)
# OR
read(<user input>)
```

**Exemplo:**

```text
nome = read("Informe seu nome: ")
write("Seu nome é ${nome}.")

# Output
# Foi digitado Júlio no terminal
> Informe seu nome: Júlio
> Seu nome é Júlio.
```

### Parâmetros

## Console.ReadOption

## Console.ReadOptions

## Console.ReadSlider

