# Logical Operators

Kymera tem um conjunto mais completo de operadores lógicos com relação a demais linguagens. Além do formato de expressão lógica ele permite utilizar métodos que permite uma comparação de múltiplos valores.

## AND

```python
> true and true
#=> true

> false and false
#=> false

> true and fase
#=> false

> false and true
#=> false
```

Também pode ser feito em cadeia:

```python
> and(true, true, true)
#=> true

> and(true, false, true, false)
#=> false
```

## OR

```python
> true or true
#=> true

> false or false
#=> false

> true or fase
#=> true

> false or true
#=> true
```

```python
> or(false, false, false)
#=> false

> or(true, false, true, false)
#=> true
```

## XOR

```python
> true xor true
#=> false

> false xor false
#=> false

> true xor fase
#=> true

> false xor true
#=> true
```

```python
> xor(true, true, false)
#=> false
```

## NOT

```python
> not true
#=> false

> not false
#=> true
```

## NOR

```python
> true nor true
#=> false

> false nor false
#=> true

> true nor fase
#=> false

> false nor true
#=> false
```

```python
> nor(false, false, false)
#=> true

> nor(true, false, true, false)
#=> false
```

## NAND

```python
> true nand true
#=> false

> false nand false
#=> true

> true nand fase
#=> true

> false nand true
#=> true
```

Também pode ser feito em cadeia:

```python
> nand(true, true, true)
#=> false

> nand(true, false, true, false)
#=> true
```

## XNOR

```python
> true nxor true
#=> true

> false nxor false
#=> true

> true nxor fase
#=> false

> false nxor true
#=> false
```

```python
> nxor(true, true, false)
#=> true
```



