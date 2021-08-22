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

### split



### join

### toInt

```python
print('42'.toInt() is int)

# Output
> true
```

### toFloat

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

### toSet

### toDict

### toJson

```python

```



