# Functions

Uma função é definida com um identificador seguido de parênteses abrindo e fechando **()** e utiliza a notação de pascal em sua declaração.

A definição do tipo de retorno é opcional, caso não informe nada, ele utilizará como padrão o tipo **void**.

**Syntax:**

```kotlin
fun <identificador>(<tipo> <parâmetro>) :: [tipo retorno] do
    <código>
end
```

**Exemplo:**

```kotlin
fun somarDoisNumeros(float num1, float num2) :: float do
    var soma = num1 + num2
    return soma
end

var valor_soma = somarDoisNumeros(10.0, 2.0)

writeln(valor_soma)

# Output
$ 12.0
```

O retorno é opcional, basta definir o tipo de retorno e ele automaticamente retornará a última linha:

```kotlin
fun somarDoisNumeros(folat num1, float num2) :: float do
    num1 + num2
end

var valor_soma = somarDoisNumeros(10.0, 2.0)

writeln(valor_soma)

# Output
$ 12.0
```

Também é possível ter **múltiplos retornos**:

```kotlin
fun swap(int num1, int num2) :: (int, int) do
    return num2, num1
end
```

```kotlin
fun swap(int num1, int num2) :: (int, int) | null do
    // Some code
end
```

Podemos trabalhar com sobre carga que funciona em cima de **pattern matching**.

```kotlin
fun log(%[ :error, string message ]) do
    writeln('Something went wrong: ${message}')
end

fun log(%[ :ok, string message ]) do
    writeln('It works: ${message}')
end
```

As funções podem ter clausula de guarda, que são decorators que definem uma condição para a função ser executada:

```kotlin
@when(idade >= 18)
fun verificaIdade(int idade) do
    writeln('Maior de idade')
end

@when(idade < 18)
fun verificaIdade(int idade) do
    writeln('Menor de idade')
end
```

Podemos trabalhar com funções anônimas:

```typescript
fn(float num1, float num2) :: float do
    num1 + num2
end
```

No caso de funções anônimas **in line**, podemos usar apenas o `, do:` com o comando a ser executado na mesma linha e o tipo de retorno se torna implícito:

```typescript
fn(float num1, float num2), do: num1 + num2
```

Para fazer o **inline return**, basta usar o _arrow function_:

```kotlin
fn(string name) => 'Hello ${name}'
```
