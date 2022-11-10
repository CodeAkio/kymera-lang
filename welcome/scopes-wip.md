# Scopes \[WIP]

Kym trabalha com 3 escopos tradicionais:

### Global

Ele é acessado de qualquer lugar do sistema.

Para definir algo como global, basta usar a keywork `global`.

Apesar dele existir, deve ser usado com muita cautela, na dúvida, não use ele.

```csharp
# main.kym

global name string

fun main():
    ...
```

```csharp
# person.kym

name = "Pedro"
```

### Bloco

### Função
