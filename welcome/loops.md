---
description: The parenthesis is optional to pass expression.
---

# Loops

## For

Ele lembra muito o for do Go, porém note que ele usa `,` no lugar de `;` para separar os parâmetros para manter uma assinatura mais uniforme com outras funções.

{% hint style="info" %}
Utilize os métodos **each** e **map** quando possível, deixe o for apenas para casos especiais.
{% endhint %}

```csharp
for index := 1, index <= 10, index++ {
    writeln(index)
}

# Output
> 1
> 2
> 3
> 4
> 5
> 6
> 7
> 8
> 9
> 10
```

O for é **flexível** e não há a necessidade de ter outras estruturas como ~~while~~ ou ~~loop~~ assim como o Go, podemos obter o mesmo comportamento **alterando o número de parâmetros** passados.

Quando passamos apenas **um parâmetro**, ele recebe apenas a **condição de parada**.

Isso faz com que ele se comporte como o while tradicional.

```csharp
number := 1

for number <= 10 {
    writeln(number)
    number++
}

# Output
> 1
> 2
> 3
> 4
> 5
> 6
> 7
> 8
> 9
> 10
```

Podemos passar **dois parâmetros** apenas, neles caso ele receberá a **inicialização** e a **condição de parada**.

Ele terá o comportamento de um while, mas com a possibilidade de inicializar o valor dentro da própria estrutura

```csharp
for number := 1, number <= 10 {
    writeln(number)
    number++
}

# Output
> 1
> 2
> 3
> 4
> 5
> 6
> 7
> 8
> 9
> 10
```

Caso não passe nenhum parâmetro, ele se comporta como um **loop infinito** e só para quando receber um **break**.

```csharp
for {
    writeln('In loop...')
}
```

Também podemos fazer em **uma linha**, para isso é obrigatório o uso de **parêntese** e omitir as ~~chaves~~.

```go
for (index := 1, index <= 10, index++) writeln(index)
```

```go
for() writeln('In loop...')
```

Podemos ainda passar uma expressão usando `in`.

```ruby
for number in 1..5 {
    writeln(number)
}

# Output
> 1
> 2
> 3
> 4
> 5
```

