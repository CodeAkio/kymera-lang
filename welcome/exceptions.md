# Try / Catch

O tratamento de erros foi fortemente baseado no Python.

Podemos usar o `try` para testar o trecho de código que pode causar erro.

O `except` é executado em caso de erro.

O `finally` (opcional) é executado em tanto no se der certo ou se der erro, muito comum de ser usado para fechar conexão com banco ou fechar um arquivo.

```python
try:
    writeln(2 / 0)
except:
    ZeroDivisionError -> writeln("You cannot divide any number by zero")
finally:
    writeln("Bye!")
```

O except precisa de uma atenção especial aqui, pois tem várias formas de uso.

Podemos ter vários dele para tratar erros diferentes:

```python
try:
    # Do something
except:
    ZeroDivisionError -> writeln("You cannot divide any number by zero")
except ValueError:
    writeln("It expect a number as input")
```

Quando usamos o `else` no lugar do tipo de erro para ele, ele trata qualquer tipo de erro:

```python
try:
    # Do something
except:
    else -> writeln("There's something wrong")
```

Podemos passar como segundo parâmetro o nome do objeto que vai receber o código e mensagem do erro.

```python
try:
    # Do something
except:
    ValueError, error -> 
        writeln(error.code)
        writeln(error.message)
```

Ou ainda poderá usar pattern matching:

```python
try:
    # Do something
except:
    ValueError, %Error{code, message} ->
        writeln(code)
        writeln(message)
```

Também podemos passar um Set de erros que serão capturados pela mesma except:

```python
try:
    # Do something
except:
    (ZeroDivisionError, ValueError), errors -> writeln("Invalid input")
    else -> writeln("There's something wrong")
```
