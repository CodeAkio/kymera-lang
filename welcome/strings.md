# Strings

## Declaração

Uma string pode ser declarada entre `"` \(aspas duplas\), `'` \(aspas simples\) ou ainda ````` \(crase\).

Tente segui a convenção de utilizar as **aspas simples** para a maioria dos casos:

```python
print('Hello Kym!')

# Output
> Hello Kym!
```

Quando existe aspas simples no meio do texto, então utilize as **aspas duplas**.

```python
print("What's your name?")

# Output
> What's your name?
```

Quando precisar de uma string de _múltiplas linhas_ use a **crase**:

```javascript
print(`
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
name := 'Kym'

print('Hello ${name}')

# Output
> Hello Kym
```

## Operações com String

Assim como Python e Ruby, podemos utilizar operações aritméticas com strings.

### Concatenação

Podemos utilizar o + para unir duas strings:

```python
name := 'Kym'

print('Hello ' + name)

# Output
> Hello Kym
```

Também pode ser feito com uma string e outro tipo de valor:

```python
age := 20

print('He is ' + age + ' years old')

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

## Métodos

A string vem com uma grande começão de métodos para nos auxiliar.

{% hint style="info" %}
Todos os métodos também podem ser usados no formato **String.metodo\('valor'\)**.  
Isso dá uma grande flexibilidade quando for utilizar o _pipe operator_.
{% endhint %}

### split

Separar a string baseado em um separador do tipo string, retornando um _List&lt;string&gt;_.

```python
print('Hello Kym!'.split(' '))

# Output
> ['Hello', 'Kym!']
```

Se não passar nenhum separador, ele retorna cada um dos caracteres.

```python
print('Hello Kym!'.split())

# Output
> ['H', 'e', 'l', 'l', 'o', ' ', 'K', 'y', 'm', '!']
```

### join

Ele une um array de strings, adicionando um separador entra cada elemento.

```python
print(['Hello', 'Kym!'].join(' '))

# Output
> 'Hello Kym!'
```

### toChar

```python
print('a'.char() is char)

# Output
> true
```

### toInt

Por padrão converte para _int32_, mas é possível usar os específicos: `toInt8`, `toInt16`, `toInt32`, `toInt64`, `toUInt8`, `toUInt16`, `toUInt32`, `toUInt64`.

```python
print('42'.toInt() is int)

# Output
> true
```

### toFloat

Por padrão converte para _float32_, mas é possível usar os específicos: `toFloat32`, `toInt64`.

```python
print('42'.toFloat() is float)

# Output
> true
```

### toBool

```python
print('a'.toBool())

# Output
> true
```

### toList

Converte para um _List&lt;dynamic&gt;_.

```python
print('[1,2,3]'.toList() is List)

# Output
> true
```

### toSet

Converte para um _Set&lt;dynamic&gt;_.

```python
print('(1,2,3)'.toSet() is Set)

# Output
> true
```

### toDict

Converte para um _Dict&lt;dynamic&gt;_.

```python
print('{ name: "Kym", age: "20" }'.toDict() is Dict)

# Output
> true
```

### toUpper

```python
print('Hello Kym!'.toUpper())

# Output
> 'HELLO KYM!'
```

### toLower

```python
print('Hello Kym!'.toLower())

# Output
> 'hello kym!'
```

### toCapital

```python
print('hello kym!'.toCapital())

# Output
> 'Hello Kym!'
```

### toSnake

```python
print('Hello Kym!'.toSnake())

# Output
> 'hello_kym'
```

### toPascal

```python
print('Hello Kym!'.toPascal())

# Output
> 'HelloKym'
```

### toSkewer

```python
print('Hello Kym!'.toSkewer())

# Output
> 'hello-kym'
```

### toScreamingSnake

```python
print('Hello Kym!'.toScreamingSnake())

# Output
> 'HELLO_KYM'
```

