# Access Modifiers

Os acessos são controlados a nível de pacote que nem no Go, Dart e Rust, por padrão tudo é público e possui apenas 2 modificadores:

* **pub** (padrão) - Torna visível para fora do pacote;
* **priv** - Torna acessível somente dentro do pacote.

```kotlin
// Privado
priv fun checkValid()
    ...
end
```

```rust
// Público (padrão)
const BASE_URL = 'http://localhost:3000'
```
