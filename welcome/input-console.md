---
description: Comandos de entrada pelo console
---

# Input Console

A classe Console possui vários métodos úteis para ler os dados informados pelo usuário.  
Estes métodos podem ser chamados sem precisar explicitar a classe Console, através de seus sugar syntax.

**Exemplo:**

```text
Console.read() #Forma explicita
read() #sugar syntax de Console.read()
```

Recomenda-se que utilize o sugar syntax por ser menos verboso e natural para ler.

## Console.read

O método Read serve para possibilitar a entrada de dados do usuário pelo teclado e retorna uma string do que foi digitado.

O método Read pode receber opcionalmente uma string como argumento. Esta string será mostrada no terminal antes da leitura de dados.

**Syntax:**

```text
Console.read(<user input>)
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

Existem vários parâmetros utilizados pelo método read:

#### &lt;type&gt;

É possível definir qual o tipo de dado é aceito como entrada passando o tipo no parâmetro no formato de simbolo.  
Definido um tipo além de restringir o tipo de dado a ser aceito como entrada, o método read em vez de retornar uma string, ele retornará o valor recebido com o tipo de dado definido, ou seja, se definir o tipo como inteiro, ele só aceita números inteiros e retorna inteiros.  
Caso informe um tipo de dado diferente do suportado, será retornado uma exceção do tipo TypeError.

```text
name = read('What's your name?', :string) # Jorge
age = read('How old are you?', :int) # 23
gender = read('Are you man(M) or woman(W)?', :char) # M

write(name) 
write(age)
write(gender)

# Output
> "Jorge"
> 23
> 'M'
```

## Console.ReadOption

## Console.ReadOptions

## Console.ReadSlider

