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
    constructor(pub string nome, pub int idade) end
end
```

```ruby
class Pessoa(priv string nome, priv int idade) do
    ...
end
```

```ruby
class Pessoa(priv string nome, priv int idade) do
    get nome() :: string do
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
    constructor(priv string nome, priv int idade, priv string cpf) end
    constructor.juridica(priv string nome, priv string cnpj) end
end
```

```ruby
class Cachorro < Animal do
    constructor() end
end
```
