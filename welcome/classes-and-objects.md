---
description: Junta o Dart, Kotlin e C#
---

# Classes & Objects

## Sintaxe

```ruby
class Pessoa
    string nome
    int idade

    constructor(string nome, int idade)
        this.nome = nome
        this.idade = idade
    end
    
    fun ola() :: void
        writeln('Olá ${this.nome}')
    end
end
```

```ruby
class Pessoa
    constructor(pub string nome, pub int idade) end
end
```

```ruby
class Pessoa(priv string nome, priv int idade)
    ...
end
```

```ruby
class Pessoa(priv string nome, priv int idade)
    get nome() :: string
        return this.nome.toUpper()
    end
    
    set nome(nome)
        if nome.len() < 100 then
            this.nome = nome
        end
    end
end
```

```ruby
class Pessoa
    constructor(priv string nome, priv int idade, priv string cpf) end
    constructor.juridica(priv string nome, priv string cnpj) end
end
```

```ruby
class Cachorro < Animal
    constructor() end
end
```
