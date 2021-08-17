---
description: 'The parenthesis is optional to pass expression:'
---

# Loops

## For

```csharp
for index := 1; index <= 10; index++ {
    writeln(index)
}

# Output
> 1
> 2
> 3
> 4
> 5
> 6
> 7
> 8
> 9
> 10
```

## For in

```csharp
List<int> numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

for number in numbers {
    writeln(number)
}

# Output
> 1
> 2
> 3
> 4
> 5
> 6
> 7
> 8
> 9
> 10
```

## While

```csharp
int number = 1

while number <= 10 {
    writeln(number)
    number++
}

# Output
> 1
> 2
> 3
> 4
> 5
> 6
> 7
> 8
> 9
> 10
```

## Do while

```csharp
int number = 1

do {
    writeln(number)
    number++
} while number <= 10
```

## Loop

```rust
loop {
    writeln("In loop...")
}
```

