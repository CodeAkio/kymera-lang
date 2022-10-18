---
description: Junta o Dart, Kotlin e C#
---

# Class \[WIP]

## Sintaxe

```kotlin
class Pessoa
    nome string
    idade int

    _init(nome string, idade int)
        this.nome = nome
        this.idade = idade
    end
    
    fun ola()
        writeln("Olá ${this.nome}")
    end
end
```

```kotlin
class Pessoa
    nome string
    idade int

    _init(this.nome, this.idade) end
    
    fun ola()
        writeln("Olá ${this.nome}")
    end
end
```

```ruby
class Pessoa
    _init(pub nome string, pub idade int) end
end
```

```ruby
class Pessoa(priv nome string, priv idade int) end
```

```ruby
class Pessoa(priv nome string, priv idade int)
    get nome() :: string
        return this.nome.toUpper()
    end
    
    set nome(nome)
        if nome.len() < 100
            this.nome = nome
        end
    end
end
```

```ruby
class Pessoa
    _init(priv nome string, priv idade int, priv cpf string) end
    _init.juridica(priv nome string, priv cnpj string) end
end
```

```kotlin
class Cachorro is Animal
    _init() end
end
```

```kotlin
class Database
    ...
    _destroy()
        db.close()
    end
end
```
