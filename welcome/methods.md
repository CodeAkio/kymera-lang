# Functions

Uma função é definida com um identificador seguido de parênteses abrindo e fechando **()** e utiliza a notação de pascal em sua declaração.

A definição do tipo de retorno é opcional, caso não informe nada, ele utilizará como padrão o tipo **void**.

Os blocos são definidos com `do` e `end`, sendo o `do` opcional e somente indicado o seu uso em casos especiais.

**Syntax:**

```kotlin
fun <identificador>(<tipo> <parâmetro>) :: [tipo retorno] [do]
    <código>
end
```

**Exemplo:**

```kotlin
fun somarDoisNumeros(float num1, float num2) :: float
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
fun somarDoisNumeros(folat num1, float num2) :: float
    num1 + num2
end

var valor_soma = somarDoisNumeros(10.0, 2.0)

writeln(valor_soma)

# Output
$ 12.0
```

Também é possível ter **múltiplos retornos**:

```kotlin
fun swap(int num1, int num2) :: (int, int)
    return num2, num1
end
```

```kotlin
fun swap(int num1, int num2) :: (int, int) | null
    // Some code
end
```

Podemos trabalhar com sobre carga que funciona em cima de **pattern matching**.

```kotlin
fun log(%[ :error, string message ])
    writeln('Something went wrong: ${message}')
end

fun log(%[ :ok, string message ])
    writeln('It works: ${message}')
end
```

As funções podem ter clausula de guarda, que são decorators que definem uma condição para a função ser executada:

```kotlin
@when(idade >= 18)
fun verificaIdade(int idade)
    writeln('Maior de idade')
end

@when(idade < 18)
fun verificaIdade(int idade)
    writeln('Menor de idade')
end
```

Podemos trabalhar com funções anônimas, criando funções sem identificadores:

```typescript
(float num1, float num2) :: float
    num1 + num2
end
```

Para fazer o **in line**, basta usar o _arrow function_ e o tipo de retorno se torna implícito:

```typescript
(float num1, float num2) => num1 + num2
```

```kotlin
(string name) => 'Hello ${name}'
```
