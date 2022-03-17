# Package

O código é organizado em pacotes, que representam os arquivos de um diretório.

## Declaração

Podemos definir o nome do pacote através da keyword **package** seguido do **nome do pacote**.

Existem algumas regras de nomenclatura para pacotes:

* Deve ter o mesmo nome da pasta em que se encontra;
* Poderá usar apenas caracteres alfanuméricos e underline;
* Deve ser no formato de caixa baixa;
* Não deve ter espaço no nome, utilize o underline para isto.

```kotlin
package hello

fun Greeting() {
    writeln 'Hello'
}
```

Existe uma pacote especial que é o **main**, ele é obrigatório, pois é por ele que a aplicação inicia a execução e obrigatoriamente ele terá um método **main**.

```kotlin
package main

fun main() {
    // Something
}
```

## Exportação

Por padrão, somente **funções**, **classes**, **interfaces**, **enums**, **constantes** e **structs** são exportados dos pacotes.

```kotlin
package hello

fun Greeting() {
    writeln 'Hello'
}
```

```kotlin
package colors

enum Colors {
    RED,
    GREEN,
    BLUE,
    YELLOW,
    ORANGE,
    GRAY,
    BLACK,
    WHITE,
}
```

```kotlin
package animal

interface IAnimal {
    // Something
}

class Dog < IAnimal {
    // Something
}
```

```kotlin
package secrets

const SECRET_KEY = env.master_key
```

Caso não queira que algum deles não seja exportado, deverá declara-lo como **private** ou **protected**.

```kotlin
package animal

private interface IAnimal {
    // Something
}

class Dog < IAnimal {
    // Something
}
```

## Importação

Quando se trata de pacotes padrão ou de terceiros, basta usar a keyword **import** seguindo do nome do **pacote** e o **recurso** que deseja importar:

```kotlin
import math.PI

writeln PI

# Output
> 3.141592653589793
```

Se quiser, poderá importar **todos os recursos** do pacote, bastando importar apenas o nome do pacote:

```kotlin
import math

writeln math.PI
writeln math.E

# Output
> 3.141592653589793
> 2.718281828459045
```

{% hint style="info" %}
Essa forma de importação não é indicada quando não vai usar todos os recursos.
{% endhint %}

Podemos importar também **recursos específicos** de um pacote, usando as **chaves**.

```kotlin
import math.{ PI, E }

writeln PI
writeln E

# Output
> 3.141592653589793
> 2.718281828459045
```

Podemos definir um apelido para a importação usando a keyword **as**.

```kotlin
import math.E as EULER

writeln EULER

# Output
> 2.718281828459045
```

Para importar **pacotes locais**, usamos um **ponto** antes de passar o nome do pacote:

```kotlin
import .animal.Dog

dog := Dog(name: 'Scooby Doo', age: 2)
```
