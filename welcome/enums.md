# Enums

Por padrão os enums são do tipo int32 e recebem os valores de acordo com sua posição começando do número 0.

**Exemplo:**

```java
Enum Status {
    Online,
    Offline,
    Away,
}

writeln Status.Online

# Output
> 0
```

Também é possível definir um tipo e valores manualmente a cada um deles.

**Exemplo:**

```csharp
Enum<symbol> Status {
    Online = :online,
    Offline = :offline,
    Away = :away,
}

writeln Status.Online

# Output
> :online
```
