---
description: Ele serve para criar encadeamentos de funções.
---

# Pipe Operator

A ideia vem do Elixir, usando o operador `|>` podemos pegar o valor passando para ele e jogar como primeiro parâmetro da função que está posterior a ele.

```elixir
read_user_name()
|> clean_user_input()
|> show_greeting()
```



