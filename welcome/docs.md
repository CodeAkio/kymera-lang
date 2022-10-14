---
description: Criando documentação.
---

# Docs

Muitas documentações de código geram uma enorme sujeira, dessa forma foi criado o decorator `@doc` para documentação de classes e funções que aponta para um arquivo **docs/\*\*/\*.yml**.

A pasta **docs/** é organizada por pastas e arquivos com o mesmo nome dos pacotes.

```yaml
# docs/operations.yml

sum_numbers:
  type: fun
  description: Add two numbers
  params:
    num1:
      type: float
      description: First number to sum
    num2:
      type: float
      description: Second number to sum
  return:
    type: float
    description: Sum of two numbers
```

```kotlin
package operations

@doc("operations.sum_numbers")
fun sumNumbers(num1, num2 float) :: float
    num1 + num2
end
```

Também pode ser feito de forma implícita através da convenção do nome de pacotes e funções:

```kotlin
package operations

@doc()
fun sumNumbers(num1, num2 float) :: float
    num1 + num2
end
```



{% embed url="https://kotlinlang.org/docs/kotlin-doc.html" %}

{% embed url="https://docs.ansible.com/ansible/latest/reference_appendices/YAMLSyntax.html" %}

