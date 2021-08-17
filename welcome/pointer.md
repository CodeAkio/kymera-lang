---
description: Ele permite utilizar recursos de baixo nível como ponteiros que nem no C e Go.
---

# Pointer

Assim ele cria uma **variável do tipo ponteiro** para um determinado tipo:

```go
int* p = nil
```

Quando queremos pegar o endereço de memória de uma variável qualquer, usamos o **'&'** ante do nome da variável:

```go
numero := 1
int* p = nil

p = &numero

writeln(p)
writeln(&numero)

# Output
=> 0x420016058
=> 0x420016058
```

Para que a variável de ponteiro consiga se referenciar ao valor, usamos um **'\*'** na **variável**:

```go
numero := 1
int* p = nil

p = &numero

writeln(*p)
writeln(numero)

# Output
=> 1
=> 1
```

