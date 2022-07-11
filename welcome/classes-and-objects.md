---
description: Junta o Dart, Kotlin e C#
---

# Classes & Objects

## Sintaxe

```ruby
class Pessoa do
    string nome
    int idade

    constructor(string nome, int idade) do
        this.nome = nome
        this.idade = idade
    end
    
    fun ola() :: void do
        writeln('Olá ${this.nome}')
    end
end
```

```ruby
class Pessoa do
    constructor(public string nome, public int idade) end
end
```

```ruby
class Pessoa(private string nome, private int idade) do
    ...
end
```

```ruby
class Pessoa(private string nome, private int idade) do
    get nome() -> string so
        return this.nome.toUpper()
    end
    
    set nome(nome) do
        if nome.len() < 100 then
            this.nome = nome
        end
    end
end
```

```ruby
class Pessoa do
    constructor(private string nome, private int idade, private string cpf) end
    constructor.juridica(private string nome, private string cnpj) end
end
```

```ruby
class Cachorro < Animal do
    constructor() end
end
```
