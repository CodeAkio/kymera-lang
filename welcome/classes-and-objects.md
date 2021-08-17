---
description: 'Junta o Dart, Kotlin e C#'
---

# Classes & Objects

## Sintaxe

```kotlin
class Pessoa {
    constructor() {}
}
```

```kotlin
class Pessoa {
    constructor(private String nome, private int idade) {}
}
```

```kotlin
class Pessoa(private String nome, private int idade) {
    ...
}
```

```kotlin
class Pessoa(private String nome, private int idade) {
    get nome {
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
    constructor(private String nome, private int idade, private String cpf) {}
    constructor.juridica(private String nome, private String cnpj) {}
}
```

```kotlin
class Cachorro: Animal {
    constructor() {}
}
```



