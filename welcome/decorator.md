# Decorator \[WIP]

Utilize o `@` antes do nome da função para declarar um decorator:

```csharp
fun @greeting()
    writeln("Hello")
end
```

```csharp
@greeting()
fun snake()
    writeln("Snake")
end

snake()

# "Hello"
# "Snake"
```
