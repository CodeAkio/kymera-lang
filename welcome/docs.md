---
description: Criando documentação.
---

# Docs

Muitas documentações de código geram uma enorme sujeira, dessa forma foi criado o decorator `@doc` para documentação de classes e funções que aponta para um arquivo **docs/\*\*/\*.yml**.

A pasta docs/ é organizada por pastas com o mesmo nome dos pacotes e cada arquivo representa um recurso \(classe ou função\).

```yaml
# docs/operations.yml
type: fun
description: Add two numbers
params:
  num1:
    - type: float
    - description: First number to sum
  num2:
    - type: float
    - description: Second number to sum
return:
  - type: float
  - description: Sum of two numbers
```

```kotlin
@doc('operations.sum_numbers')
fun sumNumbers(float num1, float num2) {
    return num1 + num2
}
```

{% embed url="https://kotlinlang.org/docs/kotlin-doc.html" %}

{% embed url="https://docs.ansible.com/ansible/latest/reference\_appendices/YAMLSyntax.html" %}



