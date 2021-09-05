# Generator

Uma função pode retornar um `interable` com base no valores que ele "retorna" usando o `yield`. 

Esse retorno é automaticamente convertido de acordo com o tipo de retorno especificado na função com, por exemplo, `List` e `Set`.

```kotlin
numbers := 1..10

fun odd_numbers(int[] numbers) List {
    numbers.map((number) => {
        if number % 2 != 0 {
            yield number
        }
    })
}

writeln(odd_numbers())

# Output
> [1, 3, 5, 7, 9]
```

