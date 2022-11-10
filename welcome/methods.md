# Functions

Uma função é definida pela keywork `fun`, com um identificador, seguido de parênteses abrindo e fechando **()** e utiliza a notação de pascal em sua declaração.

A definição do tipo de retorno é opcional, caso não informe nada, ele utilizará como padrão o tipo **void**.

Os blocos são definidos com a abertura com `:` e o corpo pela indentação que nem o Python.

**Syntax:**

```kotlin
fun <identificador>(<parâmetro> <tipo>) -> [tipo retorno]:
    <código>
```

**Exemplo:**

```kotlin
fun somarDoisNumeros(num1 float, num2 float) -> float:
    var soma = num1 + num2
    return soma

var valor_soma = somarDoisNumeros(10.0, 2.0)

writeln(valor_soma)

# 12.0
```



O retorno é opcional, basta definir o tipo de retorno e ele automaticamente retornará a última linha:

```kotlin
fun somarDoisNumeros(num1 folat, num2 float) -> float:
    num1 + num2

var valor_soma = somarDoisNumeros(10.0, 2.0)

writeln(valor_soma)

# 12.0
```



Quando os parâmetros são do mesmo tipo, basta apenas informar no último:

```kotlin
fun somarDoisNumeros(num1, num2 float) -> float:
    num1 + num2

var valor_soma = somarDoisNumeros(10.0, 2.0)

writeln(valor_soma)

# 12.0
```



Também é possível ter **múltiplos retornos**:

```kotlin
fun swap(num1, num2 int) -> (int, int):
    return num2, num1
```

```kotlin
fun swap(num1, num2 int) -> (int, int) | null:
    # Some code
```



Podemos trabalhar com sobre carga que funciona em cima de **pattern matching**.

```kotlin
fun log(%[:error, message string]):
    writeln("Something went wrong: ${message}")

fun log(%[:ok, message string]):
    writeln("It works: ${message}")
```



As funções podem ter cláusula de guarda, que são decorators que definem uma condição para a função ser executada:

```kotlin
@when(idade >= 18)
fun verificaIdade(idade int):
    writeln("Maior de idade'")

@when(idade < 18)
fun verificaIdade(idade int):
    writeln("Menor de idade")
```



Podemos trabalhar com funções anônimas, criando funções sem identificadores:

```typescript
(num1, num2 float) -> float:
    num1 + num2
```



Para fazer o **in line**, basta usar o _arrow function_ e o tipo de retorno se torna implícito:

```typescript
(num1, num2 float) => num1 + num2
```

```kotlin
(name string) => "Hello ${name}"
```
