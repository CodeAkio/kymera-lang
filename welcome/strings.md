# Strings

{% hint style="info" %}
Ele é uma variação de **List\<char>**, então possui todos os recursos de um List.
{% endhint %}

## Declaração

Uma string pode ser declarada entre aspas duplas (`"`) ou aspas simples (`'`).

Para especificar seu tipo, use a keywork `string`.

```csharp
text string = "Hello Kym!"
writeln(text)

# Hello Kym!
```

<pre class="language-csharp"><code class="lang-csharp"><strong>let text = "It's awesome!"
</strong><strong>writeln(text)
</strong>
# It's awesome!
</code></pre>

```csharp
writeln('Ever ask "why"')

# Ever ask "why"
```



Quando precisar de uma string de _múltiplas linhas_ basta apenas quebrar a linha e só fechar as aspas no final:

```kotlin
writeln("
Make it work;
Make it right;
Make it fast.
")

# Make it work;
Make it right;
Make it fast.
```

## Interpolação de Strings

Para interpolar strings, basta passar o valor dentro de `${}`.

```kotlin
name := "Kym"

writeln("Hello ${name}")

# Hello Kym
```

## Operações com String

Assim como Python e Ruby, podemos utilizar operações aritméticas com strings.

### Concatenação

Podemos utilizar o + para unir duas strings:

```kotlin
name := "Kym"

writeln("Hello " + name)

# Hello Kym
```

Também pode ser feito com uma string e outro tipo de valor:

```kotlin
age := 20

writeln("He is " + age + " years old")

# He is 20 years old
```

{% hint style="info" %}
Dê preferência em utiliza _string interpolation_.
{% endhint %}

### Multiplicação

Podemos repetir uma string x vezes:

```python
"-" * 5

# "-----"
```

## Posição

Podemos acessar cada letra como um _List_.

```kotlin
some_text := "Hello Kym!"
writeln(some_text[1])

# "e"
```

Ao passar a posição negativa, ele conta da esquerda para direita:

```kotlin
some_text := "Hello Kym!"
writeln(some_text[-1])

# "m"
```

Podemos iterar como um List:

```kotlin
some_text := "Hello Kym!"

some_text.each(c => writeln(c))

# "H"
# "e"
# "l"
# "l"
# "o"
# " "
# "K"
# "y"
# "m"
# "!"
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

# 10
```

### count

Conta quantas vezes uma string se repete dentre de outra string.

```kotlin
writeln("Hello Kym!".count('l'))

# 2
```

### in

Verifica se uma string está contida em outra.

```kotlin
writeln("Kym" in "Hello Kym!")

# true
```

### contains

Similar ao in.

```kotlin
writeln("Hello Kym!".contains("Kym"))

# true
```

### split

Separar a string baseado em um separador do tipo string, retornando um _List\<string>_.

```kotlin
writeln("Hello Kym!".split(" "))

# ["Hello", "Kym!"]
```

Se não passar nenhum separador, ele retorna cada um dos caracteres.

```kotlin
writeln("Hello Kym!".split())

# ["H", "e", "l", "l", "o", " ", "K", "y", "m", "!"]
```

### join

Ele une um array de strings, adicionando um separador entra cada elemento.

```kotlin
writeln(["Hello", "Kym!"].join(" "))

# "Hello Kym!"
```

### replace

Ele substitui trechos que batem com a string ou regex.

```kotlin
var result = "Hello Kym!".replace("o", "0")

writeln(result)

# "Hell0 Kym!"
```

```kotlin
var result = "Hello Kym!".replace(re"[aeiou]", "0")

writeln(result)

# "H0ll0 Kym!"
```

### startsWith

```kotlin
var result = "Hello Friend!".startsWith("He")

writeln(result)

# true
```

### endsWith

```kotlin
var result = "Hello Friend!".endsWith("!")

writeln(result)

# true
```

### toChar

```kotlin
writeln("a".toChar() is char)

# true
```

### toInt

Por padrão converte para _int32_, mas é possível usar os específicos: `toInt8`, `toInt16`, `toInt32`, `toInt64`, `toUInt8`, `toUInt16`, `toUInt32`, `toUInt64`.

```kotlin
writeln("42".toInt() is int)

# true
```

### toFloat

Por padrão converte para _float32_, mas é possível usar os específicos: `toFloat32`, `toInt64`.

```kotlin
writeln("42".toFloat() is float)

# true
```

### toBool

```kotlin
writeln("a".toBool())

# true
```

### toList

Converte para um _List\<dynamic>_.

```kotlin
writeln("[1,2,3]".toList() is List)

# true
```

### toSet

Converte para um _Set\<dynamic>_.

```kotlin
writeln("(1,2,3)".toSet() is Set)

# true
```

### toMap

Converte para um Map_\<dynamic>_.

```kotlin
writeln("{ name: \"Kym\", age: \"20\" }".toMap() is Map)

# true
```

### toUpper

```kotlin
writeln("Hello Kym!".toUpper())

# "HELLO KYM!"
```

### toLower

```kotlin
writeln("Hello Kym!".toLower())

# "hello kym!"
```

### toCapital

```kotlin
writeln("hello kym!".toCapital())

# "Hello Kym!"
```

### toSnake

```kotlin
writeln("Hello Kym!".toSnake())

# "hello_kym"
```

### toPascal

```kotlin
writeln("Hello Kym!".toPascal())

# "HelloKym"
```

### toSkewer

```kotlin
writeln("Hello Kym!".toSkewer())

# "hello-kym"
```

### toScreamingSnake

```kotlin
writeln("Hello Kym!".toScreamingSnake())

# "HELLO_KYM"
```

{% embed url="https://ruby-doc.org/core-3.0.2/String.html" %}

{% embed url="https://docs.python.org/pt-br/3/library/string.html" %}

