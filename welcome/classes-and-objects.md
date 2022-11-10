---
description: Junta o Dart, Kotlin e C#
---

# Class \[WIP]

## Sintaxe

```kotlin
class Pessoa:
    nome string
    idade int

    _init(nome string, idade int):
        this.nome = nome
        this.idade = idade
    
    fun ola():
        writeln("Olá ${this.nome}")
```

```kotlin
class Pessoa:
    nome string
    idade int

    _init(this.nome, this.idade)
    
    fun ola():
        writeln("Olá ${this.nome}")
```

```ruby
class Pessoa:
    _init(pub nome string, pub idade int)
```

```ruby
class Pessoa(priv nome string, priv idade int)
```

```ruby
class Pessoa(priv nome string, priv idade int):
    get nome() :: string:
        return this.nome.toUpper()
    
    set nome(nome):
        if nome.len() < 100:
            this.nome = nome
```

```ruby
class Pessoa:
    _init(priv nome string, priv idade int, priv cpf string)
    _init.juridica(priv nome string, priv cnpj string)
```

```kotlin
class Database:
    ...
    _destroy():
        db.close()
```
