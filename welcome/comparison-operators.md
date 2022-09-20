# Comparison Operators

## Igual

```ruby
> 10 == '10'
=> false

> 10 == 10.0
=> false

> 10 == 10
=> true
```

Ou a forma verbal:

```ruby
> 10 eql '10'
=> false

> 10 eql 10.0
=> false

> 10 eql 10
=> true
```

## Igual (tipo diferente)

```go
$ 10 ~= '10'
=> true

$ 10 ~= 10.0
=> true

$ 10 ~= 10
=> true
```

## Diferente

```python
$ 10 != '10'
# true

$ 10 != 10.0
# true

$ 10 != 10
# false
```

Ou a forma verbal:

```ruby
> 10 not eql '10'
=> false

> 10 not eql 10.0
=> false

> 10 not eql 10
=> true
```

## Maior

```ruby
$ 10 > 10
# false

$ 100 > 10
# true

$ 10.0 > 10
# false

$ 'b' > 'a'
# true
```

Ou a forma verbal:

```ruby
> 10 gt '10'
=> false

> 10 gt 10.0
=> false

> 10 gt 10
=> true
```

## Menor

```python
$ 10 < 10
# false

$ 100 < 10
# true

$ 10.0 < 10
# false

$ 'b' < 'a'
# true
```

Ou a forma verbal?

```ruby
> 10 lt '10'
=> false

> 10 lt 10.0
=> false

> 10 lt 10
=> true
```
