# Decorator

Utilize o `@` antes do nome da função para declarar um decorator:

```kotlin
fun @greeting()
    writeln('Hello')
end
```

```kotlin
@greeting()
fun snake()
    writeln('Snake')
end

snake()

# Output
> 'Hello'
> 'Snake'
```
