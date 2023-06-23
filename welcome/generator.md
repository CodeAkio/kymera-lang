# Generator

Uma função pode retornar um `interable` com base nos valores que ele "retorna" usando o `yield`.&#x20;

Esse retorno é automaticamente convertido de acordo com o tipo de retorno especificado na função com, por exemplo, `List` e `Set`.

```csharp
var numbers = 1 to 10

fun odd_numbers(numbers int[]) -> List {
    numbers.each((number) => if number % 2 != 0 then yield number)
}

writeln(odd_numbers())

# [1, 3, 5, 7, 9]
```
