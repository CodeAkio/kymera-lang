# Decorator

Utilize o `@` antes do nome da função para declarar um decorator:

```kotlin
fun @greeting() {
    writeln 'Hello'
}
```

```kotlin
@greeting()
fun snake() do
    writeln 'Snake'
end

snake()

# Output
> 'Hello'
> 'Snake'
```
