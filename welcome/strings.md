# Strings

{% hint style="info" %}
Ele é uma variação de **List\<char>**, então possui todos os recursos de um List.
{% endhint %}

## Declaração

Uma string pode ser declarada entre `"` (aspas duplas).

```kotlin
writeln("Hello Kym!")

# Output
> Hello Kym!
```

Quando precisar de uma string de _múltiplas linhas_ basta apenas quebrar a linha e só fechar as aspas no final:

```kotlin
writeln("
Make it work;
Make it right;
Make it fast.
")

# Output
> Make it work;
Make it right;
Make it fast.
```

## Interpolação de Strings

Para interpolar strings, basta passar o valor dentro de `${}`.

```kotlin
var name = "Kym"

writeln("Hello ${name}")

# Output
> Hello Kym
```

## Operações com String

Assim como Python e Ruby, podemos utilizar operações aritméticas com strings.

### Concatenação

Podemos utilizar o + para unir duas strings:

```kotlin
var name = "Kym"

writeln("Hello " + name)

# Output
> Hello Kym
```

Também pode ser feito com uma string e outro tipo de valor:

```kotlin
var age = 20

writeln("He is " + age + " years old")

# Output
> He is 20 years old
```

{% hint style="info" %}
Dê preferência em utiliza _string interpolation_.
{% endhint %}

### Multiplicação

Podemos repetir uma string x vezes:

```python
"-" * 5

# Output
> "-----"
```

## Posição

Podemos acessar cada letra como um _List_.

```kotlin
var some_text = "Hello Kym!"
writeln(some_text[1])

# Output
> 'e'
```

Ao passar a posição negativa, ele conta da esquerda para direita:

```kotlin
var some_text = "Hello Kym!"
writeln(some_text[-1])

# Output
> 'm'
```

Podemos iterar como um List:

```kotlin
var some_text = "Hello Kym!"

some_text.each(c => writeln(c))

# Output
> 'H'
> 'e'
> 'l'
> 'l'
> 'o'
> ' '
> 'K'
> 'y'
> 'm'
> '!'
```

## Métodos

A string vem com uma grande começão de métodos para nos auxiliar.

{% hint style="info" %}
Todos os métodos também podem ser usados no formato **String.metodo('valor')**.\
Isso dá uma grande flexibilidade quando for utilizar o _pipe operator_.
{% endhint %}

### length

Diz quantos caracteres possui a string.

```kotlin
writeln("Hello Kym!".length)

# Output
> 10
```

### count

Conta quantas vezes uma string se repete dentre de outra string.

```kotlin
writeln("Hello Kym!".count('l'))

# Output
> 2
```

### in

Verifica se uma string está contida em outra.

```kotlin
writeln("Kym" in "Hello Kym!")

# Output
> true
```

### contains

Similar ao in.

```kotlin
writeln("Hello Kym!".contains("Kym"))

# Output
> true
```

### split

Separar a string baseado em um separador do tipo string, retornando um _List\<string>_.

```kotlin
writeln("Hello Kym!".split(' '))

# Output
> ["Hello", "Kym!"]
```

Se não passar nenhum separador, ele retorna cada um dos caracteres.

```kotlin
writeln("Hello Kym!".split())

# Output
> ['H', 'e', 'l', 'l', 'o', ' ', 'K', 'y', 'm', '!']
```

### join

Ele une um array de strings, adicionando um separador entra cada elemento.

```kotlin
writeln(["Hello", "Kym!"].join(' '))

# Output
> "Hello Kym!"
```

### replace

Ele substitui trechos que batem com a string o regex.

```kotlin
var result = "Hello Kym!".replace('o', '0')

writeln(result)

# Output
> "Hell0 Kym!"
```

```kotlin
var result = "Hello Kym!".replace(/[aeiou]/, '0')

writeln(result)

# Output
> "H0ll0 Kym!"
```

### startsWith

```kotlin
var result = "Hello Friend!".startsWith("He")

writeln(result)

# Output
> true
```

### endsWith

```kotlin
var result = "Hello Friend!".endsWith('!')

writeln(result)

# Output
> true
```

### toChar

```kotlin
writeln("a".toChar() is char)

# Output
> true
```

### toInt

Por padrão converte para _int32_, mas é possível usar os específicos: `toInt8`, `toInt16`, `toInt32`, `toInt64`, `toUInt8`, `toUInt16`, `toUInt32`, `toUInt64`.

```kotlin
writeln("42".toInt() is int)

# Output
> true
```

### toFloat

Por padrão converte para _float32_, mas é possível usar os específicos: `toFloat32`, `toInt64`.

```kotlin
writeln("42".toFloat() is float)

# Output
> true
```

### toBool

```kotlin
writeln("a".toBool())

# Output
> true
```

### toList

Converte para um _List\<dynamic>_.

```kotlin
writeln("[1,2,3]".toList() is List)

# Output
> true
```

### toSet

Converte para um _Set\<dynamic>_.

```kotlin
writeln("(1,2,3)".toSet() is Set)

# Output
> true
```

### toMap

Converte para um Map_\<dynamic>_.

```kotlin
writeln("{ name: \"Kym\", age: \"20\" }".toMap() is Map)

# Output
> true
```

### toUpper

```kotlin
writeln("Hello Kym!".toUpper())

# Output
> "HELLO KYM!"
```

### toLower

```kotlin
writeln("Hello Kym!".toLower())

# Output
> "hello kym!"
```

### toCapital

```kotlin
writeln("hello kym!".toCapital())

# Output
> "Hello Kym!"
```

### toSnake

```kotlin
writeln("Hello Kym!".toSnake())

# Output
> "hello_kym"
```

### toPascal

```kotlin
writeln("Hello Kym!".toPascal())

# Output
> "HelloKym"
```

### toSkewer

```kotlin
writeln("Hello Kym!".toSkewer())

# Output
> "hello-kym"
```

### toScreamingSnake

```kotlin
writeln("Hello Kym!".toScreamingSnake())

# Output
> "HELLO_KYM"
```

{% embed url="https://ruby-doc.org/core-3.0.2/String.html" %}

{% embed url="https://docs.python.org/pt-br/3/library/string.html" %}

