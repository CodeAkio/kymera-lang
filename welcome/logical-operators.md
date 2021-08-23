# Logical Operators

Kymera tem um conjunto mais completo de operadores lógicos com relação a demais linguagens. Além do formato de expressão lógica ele permite utilizar métodos que permite uma comparação de múltiplos valores.

## AND

```python
> true and true
true

> false and false
false

> true and fase
false

> false and true
false
```

Também pode ser feito em cadeia:

```python
> ands(true, true, true)
true

> ands(true, false, true, false)
false
```

## OR

```python
> true or true
true

> false or false
false

> true or fase
true

> false or true
true
```

```python
> ors(false, false, false)
# false

> ors(true, false, true, false)
# true
```

## XOR

```python
> true xor true
false

> false xor false
false

> true xor fase
true

> false xor true
true
```

## NOT

```python
> not true
false

> not false
true
```

## NOR

## NAND

## XNOR

