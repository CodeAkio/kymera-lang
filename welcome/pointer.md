---
description: Ele permite utilizar recursos de baixo nível como ponteiros que nem no C e Go.
---

# Pointer

Para definir uma variável que armazenará um ponteiro, basta que no tipo tenha um **'\*'** como sufixo.

Assim ele cria uma **variável do tipo ponteiro** para um determinado tipo:

```csharp
*int p = null
```

Quando queremos pegar o endereço de memória de uma variável qualquer, usamos o **'&'** ante do nome da variável:

```csharp
numero := 1
*int p = null

p = &numero

writeln p
writeln &numero

# Output
=> 0x420016058
=> 0x420016058
```

Para que a variável de ponteiro consiga se referenciar ao valor, usamos um **'\*'** na **variável**:

```csharp
numero := 1
*int p = null

p = &numero

writeln *p
writeln numero

# Output
=> 1
=> 1
```
