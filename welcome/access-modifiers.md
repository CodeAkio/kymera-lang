# Access Modifiers

Os acessos são controlados a nível de pacote que nem no Go e Rust, por padrão classes, funções, enums, interfaces são públicos e o restante é privado.

Para modificar o comportamento padrão deverá usar as keywords:

* `pub` - Público, visível fora do módulo;
* `priv` - Privado, visível apenas dentro do módulo.

```kotlin
priv fun checkValid() {
    ...
}
```

```rust
pub const BASE_URL = 'http://localhost:3000'
```
