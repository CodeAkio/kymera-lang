# Decorator \[WIP]

Utilize o `@` antes do nome da função para declarar um decorator:

```csharp
fun @greeting() {
    writeln("Hello")
}
```

```csharp
@greeting()
fun snake() {
    writeln("Snake")
}

snake()

# "Hello"
# "Snake"
```
