---
description: Junta o Dart, Kotlin e C#
---

# Classes & Objects

## Sintaxe

```kotlin
class Pessoa {
    string nome
    int idade

    constructor(string nome, int idade) {
        this.nome = nome
        this.idade = idade
    }
    
    fun ola() -> void {
        writeln 'Olá ${this.nome}'
    }
}
```

```kotlin
class Pessoa {
    constructor(public string nome, public int idade) {}
}
```

```kotlin
class Pessoa(private string nome, private int idade) {
    ...
}
```

```kotlin
class Pessoa(private string nome, private int idade) {
    get nome() -> string {
        return this.nome.toUpper()
    }
    
    set nome(nome) {
        if nome.len() < 100 {
            this.nome = nome
        }
    }
}
```

```kotlin
class Pessoa {
    constructor(private string nome, private int idade, private string cpf) {}
    constructor.juridica(private string nome, private string cnpj) {}
}
```

```kotlin
class Cachorro < Animal {
    constructor() {}
}
```
