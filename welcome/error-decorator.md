# Error Decorator

É um decorator que trata exceptions de funções pontuais, inspirado no Go e Elixir.

Dê preferência em utiliza-lo no lugar do try/catch, pois tornará o código mais resiliente e com tratamento mais preciso.

Para utiliza-lo basta decorar a chamada da função com `@error` passando a função de tratamento como parâmetro que receba como primeiro parâmetro um tipo `Error`.

Ele disponibiliza o método Return() que permite fazer o returno no escopo de onde ele é chamado.

```elixir
@error(failOnGetUsers)
var users = getValidUsers()

fun failOnGetUsers(err Error) {
    writeln("Error on get users!\n${err}")
    Return()
}
```



Caso o nome da função de tratamento seja igual à função chamadora com o sufixo \*Error, a passagem dela por parâmetro será implícita.

```elixir
@error()
var users = getValidUsers()

fun getValidUsersError(err Error) {
    writeln("Error on get users!\n${err}")
    Return()
}
```

