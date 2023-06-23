# Access Modifiers

Os acessos são controlados ao nível de módulo que nem no Go, Dart e Rust, por padrão tudo é público e possui apenas 2 modificadores:

* **pub** - Torna visível para fora do módulo;
* **priv** (padrão) - Torna acessível somente dentro do módulo.

```kotlin
// Privado
fun checkValid() {
    ...
}
```

```rust
// Público
pub const BASE_URL = "http://localhost:3000"
```
