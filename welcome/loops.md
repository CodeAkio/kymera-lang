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
for (var index = 1, index <= 10, index.inc())
    writeln(index)
end

# 1
# 2
# 3
# 4
# 5
# 6
# 7
# 8
# 9
# 10
```



O for é **flexível** e não há a necessidade de ter outras estruturas como ~~while~~ ou ~~loop~~ assim como o Go, podemos obter o mesmo comportamento **alterando o número de parâmetros** passados.

Quando passamos apenas **um parâmetro**, ele recebe apenas a **condição de parada**.

Isso faz com que ele se comporte como o while tradicional.

```csharp
var number = 1

for number <= 10
    writeln(number)
    number.inc()
end

# 1
# 2
# 3
# 4
# 5
# 6
# 7
# 8
# 9
# 10
```



Podemos passar **dois parâmetros** apenas, neles caso ele receberá a **inicialização** e a **condição de parada**.

Ele terá o comportamento de um while, mas com a possibilidade de inicializar o valor dentro da própria estrutura

```csharp
for (var number = 1, number <= 10)
    writeln(number)
    number.inc()
end

# 1
# 2
# 3
# 4
# 5
# 6
# 7
# 8
# 9
# 10
```



Também podemos fazer em **uma linha**, para isso utilize arrow function.

```kotlin
for (var index = 1, index <= 10, index.inc()) => writeln(index)
```



Podemos ainda passar uma expressão usando `in`, neste caso não precisa usar o ~~var~~.

```elixir
for number in (1 to 5) => writeln(number)

# 1
# 2
# 3
# 4
# 5
```



Para trabalhar com um **loop infinito** basta usar o `for` sem condição e só parar quando receber um `break`.

```elixir
for
    writeln("In loop...")
end
```



Também pode fazer **in line**.

```elixir
for => writeln("In loop...")
```
