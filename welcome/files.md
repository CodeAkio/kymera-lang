# Files

A biblioteca `file` possui vários métodos que ajudar a trabalhar com arquivos.

### open

O `open` abre o arquivo, por padrão considera que é um arquivo **txt** e no modo **somente leitura**:

```python
import file.*

var my_file = open('some_file.txt')
```

A propriedade `mode`, podemos passar `:r` para somente leitura e `:w` para leitura e escrita.

```python
import file.*

var my_file = open('some_file.txt', mode: :w)
```

A propriedade `type`, podemos passar `:txt`para arquivos do tipo texto, ou `:bin` para arquivos do tipo binário.

```python
import file.*

var my_file = open('some_file.txt', type: :txt)
```

A propriedade `mode`, podemos passar `:a` para escrever as mudanças apenas no fim do arquivo, ou `:e` para sobrescrever o arquivo inteiro, por padrão ele trabalha com `:e`.

```python
import file.*

var my_file = open('some_file.txt', mode: :a)
```

### close

Após abrir o arquivo, precisamos fecha-lo para que ele não fique bloqueado.

```python
import file.*

try
    var my_file = open('some_file.txt')
except
    FileNotFoundError, error -> writeln error
finally
    my_file.close()
end
```

### read

### readlines

[https://www.rubyguides.com/2015/05/working-with-files-ruby/](https://www.rubyguides.com/2015/05/working-with-files-ruby/)
