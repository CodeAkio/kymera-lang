# Enums

Por padrão os enums são do tipo int32 e recebem os valores de acordo com sua posição começando do número 0.

```java
enum Status:
    Online
    Offline
    Away

writeln(Status.Online)

# 0
```



Pode definir um tipo e valores manualmente a cada um deles.

```csharp
enum Status symbol:
    Online = :online
    Offline = :offline
    Away = :away

writeln(Status.Online)

# :online
```
