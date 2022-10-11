# Comparison Operators

## Igual

```ruby
10 == "10"
# false

10 == 10.0
# false

10 == 10
# true
```

Ou a forma verbal:

```ruby
10 eql "10"
# false

10 eql 10.0
# false

10 eql 10
# true
```

## Igual (tipo diferente)

```python
10 ~= "10"
# true

10 ~= 10.0
# true

10 ~= 10
# true
```

## Diferente

```python
10 != "10"
# true

10 != 10.0
# true

10 != 10
# false
```

Ou a forma verbal:

```ruby
10 not eql "10"
# false

10 not eql 10.0
# false

10 not eql 10
# true
```

## Maior

```ruby
10 > 10
# false

100 > 10
# true

10.0 > 10
# false

"b" > "a"
# true
```

Ou a forma verbal:

```ruby
10 gt 10
# false

10 gt 12
# false

10 gt 7
# true
```

### Maior ou Igual

```ruby
10 >= 10
# true

100 >= 10
# true

10.0 >= 10
# true

"b" >= "a"
# true
```

Ou a forma verbal:

```ruby
10 gte 10
# true

10 gte 12
# false

10 gte 7
# true
```

## Menor

```python
10 < 10
# false

2 < 10
# true

100 < 10
# false

10.0 < 10
# false

"b" < "a"
# true
```

Ou a forma verbal?

```ruby
10 lt 10
# false

10 lt 12
# true

10 lt 7
# false
```

### Menor ou Igual

```python
10 <= 10
# true

2 <= 10
# true

100 <= 10
# false

10.0 <= 10
# true

"b" <= "a"
# true
```

Ou a forma verbal?

```ruby
10 lte 10
# true

10 lte 12
# true

10 lte 7
# false
```

