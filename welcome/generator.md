# Generator

Uma função pode retornar um `interable` com base no valores que ele "retorna" usando o `yield`.&#x20;

Esse retorno é automaticamente convertido de acordo com o tipo de retorno especificado na função com, por exemplo, `List` e `Set`.

```kotlin
var numbers = 1 to 10

fun odd_numbers(int[] numbers) -> List do
    numbers.each(fn(number) do
        if number % 2 != 0 do
            yield number
        end
    end)
end

writeln(odd_numbers())

# Output
> [1, 3, 5, 7, 9]
```
