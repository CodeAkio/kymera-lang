# Access Modifiers

Os acessos são controlados ao nível de módulo que nem no Go, Dart e Rust, por padrão tudo é público e possui apenas 2 modificadores:

* **pub** (padrão) - Torna visível para fora do módulo;
* **priv** - Torna acessível somente dentro do módulo.

```kotlin
// Privado
priv fun checkValid()
    ...
end
```

```rust
// Público (padrão)
BASE_URL = "http://localhost:3000"
```
