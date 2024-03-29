---
description: Ele permite utilizar recursos de baixo nível como ponteiros que nem no C e Go.
---

# Pointer

Para definir uma variável que armazenará um ponteiro, basta usar a kword **'ref'**.

Assim ele cria uma **variável do tipo ponteiro** para um determinado tipo:

```csharp
ref p int = null
```

Quando queremos pegar o endereço de memória de uma variável qualquer, usamos o **'&'** ante do nome da variável:

```csharp
var numero = 1
ref p int = null

p = &numero

writeln(p)
writeln(&numero)

# 0x420016058
# 0x420016058
```

Para que a variável de ponteiro consiga se referenciar ao valor, usamos um **'\*'** na **variável**:

```csharp
var numero = 1
ref p int = null

p = &numero

writeln(*p)
writeln(numero)

# 1
# 1
```
