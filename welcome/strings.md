# Strings

{% hint style="info" %}
Ele é uma variação de **List\<char>**, então possui todos os recursos de um List.
{% endhint %}

## Declaração

Uma string pode ser declarada entre `"` (aspas duplas), `'` (aspas simples) ou ainda `` ` `` (crase).

Tente segui a convenção de utilizar as **aspas simples** para a maioria dos casos:

```python
writeln 'Hello Kym!'

# Output
> Hello Kym!
```

Quando existe aspas simples no meio do texto, então utilize as **aspas duplas**.

```python
writeln "What's your name?"

# Output
> What's your name?
```

Quando precisar de uma string de _múltiplas linhas_ use a **crase**:

```javascript
writeln(`
Make it work;
Make it right;
Make it fast.
`)

# Output
> Make it work;
Make it right;
Make it fast.
```

## Interpolação de Strings

Para interpolar strings, basta passar o valor dentro de `${}`.

```typescript
var name = 'Kym'

writeln 'Hello ${name}'

# Output
> Hello Kym
```

## Operações com String

Assim como Python e Ruby, podemos utilizar operações aritméticas com strings.

### Concatenação

Podemos utilizar o + para unir duas strings:

```python
var name = 'Kym'

writeln('Hello ' + name)

# Output
> Hello Kym
```

Também pode ser feito com uma string e outro tipo de valor:

```python
var age = 20

writeln('He is ' + age + ' years old')

# Output
> He is 20 years old
```

{% hint style="info" %}
Dê preferência em utiliza _string interpolation_.
{% endhint %}

### Multiplicação

Podemos repetir uma string x vezes:

```python
'-' * 5

# Output
> '-----'
```

## Posição

Podemos acessar cada letra como um _List_.

```ruby
some_text = 'Hello Kym!'
writeln(some_text[1])

# Output
> 'e'
```

Ao passar a posição negativa, ele conta da esquerda para direita:

```ruby
some_text = 'Hello Kym!'
writeln(some_text[-1])

# Output
> 'm'
```

Podemos iterar como um List:

```ruby
some_text = 'Hello Kym!'

some_text.each(c -> writeln c)

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

```ruby
writeln 'Hello Kym!'.length

# Output
> 10
```

### count

Conta quantas vezes uma string se repete dentre de outra string.

```ruby
writeln 'Hello Kym!'.count('l')

# Output
> 2
```

### in

Verifica se uma string está contida em outra.

```ruby
writeln 'Kym' in 'Hello Kym!'

# Output
> true
```

### contains

Similar ao in.

```ruby
writeln 'Hello Kym!'.contains('Kym')

# Output
> true
```

### split

Separar a string baseado em um separador do tipo string, retornando um _List\<string>_.

```python
writeln 'Hello Kym!'.split(' ')

# Output
> ['Hello', 'Kym!']
```

Se não passar nenhum separador, ele retorna cada um dos caracteres.

```python
writeln 'Hello Kym!'.split()

# Output
> ['H', 'e', 'l', 'l', 'o', ' ', 'K', 'y', 'm', '!']
```

### join

Ele une um array de strings, adicionando um separador entra cada elemento.

```python
writeln ['Hello', 'Kym!'].join(' ')

# Output
> 'Hello Kym!'
```

### replace

Ele substitui trechos que batem com a string o regex.

```python
var result = 'Hello Kym!'.replace('o', '0')

writeln(result)

# Output
> 'Hell0 Kym!'
```

```python
var result = 'Hello Kym!'.replace(/[aeiou]/, '0')

writeln(result)

# Output
> 'H0ll0 Kym!'
```

### startsWith

```python
var result = 'Hello Friend!'.startsWith('He')

writeln(result)

# Output
> true
```

### endsWith

```python
var result = 'Hello Friend!'.endsWith('!')

writeln(result)

# Output
> true
```

### toChar

```python
writeln('a'.char() is char)

# Output
> true
```

### toInt

Por padrão converte para _int32_, mas é possível usar os específicos: `toInt8`, `toInt16`, `toInt32`, `toInt64`, `toUInt8`, `toUInt16`, `toUInt32`, `toUInt64`.

```python
writeln('42'.toInt() is int)

# Output
> true
```

### toFloat

Por padrão converte para _float32_, mas é possível usar os específicos: `toFloat32`, `toInt64`.

```python
writeln('42'.toFloat() is float)

# Output
> true
```

### toBool

```python
writeln('a'.toBool())

# Output
> true
```

### toList

Converte para um _List\<dynamic>_.

```python
writeln('[1,2,3]'.toList() is List)

# Output
> true
```

### toSet

Converte para um _Set\<dynamic>_.

```python
writeln('(1,2,3)'.toSet() is Set)

# Output
> true
```

### toDict

Converte para um _Dict\<dynamic>_.

```python
writeln('{ name: "Kym", age: "20" }'.toDict() is Dict)

# Output
> true
```

### toUpper

```python
writeln('Hello Kym!'.toUpper())

# Output
> 'HELLO KYM!'
```

### toLower

```python
writeln('Hello Kym!'.toLower())

# Output
> 'hello kym!'
```

### toCapital

```python
writeln('hello kym!'.toCapital())

# Output
> 'Hello Kym!'
```

### toSnake

```python
writeln('Hello Kym!'.toSnake())

# Output
> 'hello_kym'
```

### toPascal

```python
writeln('Hello Kym!'.toPascal())

# Output
> 'HelloKym'
```

### toSkewer

```python
writeln('Hello Kym!'.toSkewer())

# Output
> 'hello-kym'
```

### toScreamingSnake

```python
writeln('Hello Kym!'.toScreamingSnake())

# Output
> 'HELLO_KYM'
```

{% embed url="https://ruby-doc.org/core-3.0.2/String.html" %}

{% embed url="https://docs.python.org/pt-br/3/library/string.html" %}

