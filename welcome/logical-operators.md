# Logical Operators

Kymera tem um conjunto mais completo de operadores lógicos com relação a demais linguagens. Além do formato de expressão lógica ele permite utilizar métodos que permite uma comparação de múltiplos valores.

## AND

```text
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

```text
> ands(true, true, true)
true

> ands(true, false, true, false)
false
```

## OR

```text
> true or true
true

> false or false
false

> true or fase
true

> false or true
true
```

## XOR

```text
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

```text
> not true
false

> not false
true
```

## NOR

## NAND

## XNOR

