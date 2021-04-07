# Enums

Por padrão os enums são do tipo int32 e recebem os valores de acordo com sua posição começando do número 0.

**Exemplo:**

```text
enum Status {
    Online,
    Offline,
    Away,
}

write(Status.Online)

# Output
> 0
```

Também é possível definir um tipo e valores manualmente a cada um deles.

**Exemplo:**

```text
enum Status<Symbol> {
    Online = :online,
    Offline = :offline,
    Away = :away,
}

write(Status.Online)

# Output
> :online
```

