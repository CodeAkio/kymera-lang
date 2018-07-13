---
description: Como utilizar a interface IList
---

# List

## Introdução

A interface IList permite armazenar vários valores de diferentes tipos que podem ser acessados através de um índice número que começa com o número 0. Esses múltiplos valores são armazenados em uma variável ou uma contante do tipo IList.

A estrutura de dados List é uma interface chamada IList, porém para fins de simplicidade poderá e é recomendado utilizar no sistema pelo sugar syntax List.

Kymera não trabalha com a estrutura de dados do tipo array, pois a estrutura de dados de uma list tem mais recursos e flexibilidade do que o array.

## Declaração e Atribuição

A declaração de uma variável ou contante List pode ser feito de forma duas formas

* **Explícita:** Deverá definir o tipo de variável explicitamente como List.

```text
List fruit
fruit = ['Apple', 'Orange', 'Banana']
```

* **Implícita:** Basta atribuir diretamente os valores a variável e o interpretador vai declara-lo implicitamente como List, sendo que os valores ficaram dentro dos colchetes e separados por vírgula.

```text
fruit = ['Apple', 'Orange', 'Banana']

# OR

fruit = []
```

Também é possível restringir o tipo de dados que a lista pode receber usando generics, dessa forma deverá usar sempre a forma explícita de declaração.  
Caso tente atribuir um valor com um tipo de dado diferente, será retornado uma exceção do tipo TypeError.

```text
List<int> numbers
numbers = [1, 2, 3, 4, 5]

write(numbers)

# Output
> [1, 2, 3, 4, 5]
```

## Methods

Uma lista possui vários métodos úteis que podem ser utilizados.

### add

### insert

### remove

### pop

### reverse

### contains?

### indexOf

### sort

### count







