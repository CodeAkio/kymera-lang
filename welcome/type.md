# Type

É possível criar tipos customizados utilizando a keyword `type`.

### Restringindo Valores

O operador (`|`) nos permite definir que uma variável pode ser mais de um tipo ou restringir os valores aceitos:

```typescript
type Status = "doing" | "pending" | "completed"

Status currentStatus = "doing" // Valid
currentStatus = "invalid" // Type Error
```

```typescript
type Rate = 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10

Rate productRate = 8 // Valid
poductRate = 0 // Type Error
```

### Restringindo Tipos

Podemos restringir que tipos ele aceita.

Para facilitar isso existem tipos genéricos como o `number` que aceita qualquer tamanho de int e float.

```typescript
type Age = number | string

Age myAge = 20 // Valid
myAge = 22.0 // Valid
myAge = "21" // Valid
myAge = Date.now() // Type Error
```
