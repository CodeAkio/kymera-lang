# Logical Operators

Kymera tem um conjunto mais completo de operadores lógicos com relação a demais linguagens. Além do formato de expressão lógica ele permite utilizar métodos que permite uma comparação de múltiplos valores.

## AND

```python
$ true and true
# true

$ false and false
# false

$ true and fase
# false

$ false and true
# false
```

Também pode ser feito em cadeia:

```python
$ and(true, true, true)
# true

$ and(true, false, true, false)
# false
```

## OR

```python
$ true or true
# true

$ false or false
# false

$ true or fase
# true

$ false or true
# true
```

```python
$ or(false, false, false)
# false

$ or(true, false, true, false)
# true
```

## XOR

```python
$ true xor true
# false

$ false xor false
# false

$ true xor fase
# true

$ false xor true
# true
```

```python
$ xor(true, true, false)
# false
```

## NOT

```python
$ not true
# false

$ not false
# true
```

## NOR

```python
$ not (true or true)
# false

$ not (false or false)
# true

$ not (true or fase)
# false

$ not (false or true)
# false
```

```python
$ not or(false, false, false)
# true

$ not or(true, false, true, false)
# false
```

## NAND

```python
$ not (true and true)
# false

$ not (false and false)
# true

$ not (true and fase)
# true

$ not (false and true)
# true
```

Também pode ser feito em cadeia:

```python
$ not and(true, true, true)
# false

$ not and(true, false, true, false)
# true
```

## XNOR

```python
$ not (true xor true)
# true

$ not (false xor false)
# true

$ not (true xor fase)
# false

$ not (false xor true)
# false
```

```python
$ not xor(true, true, false)
# true
```

