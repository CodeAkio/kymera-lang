# Files

A biblioteca `file` possui vários métodos que ajudar a trabalhar com arquivos.

### open

O `open` abre o arquivo, por padrão considera que é um arquivo **txt** e no modo **somente leitura**:

```python
import file.*

my_file := read('some_file.txt')
```

A propriedade `mode`, podemos passar `:r` para somente leitura e `:w` para leitura e escrita.

```python
import file.*

my_file := read('some_file.txt', mode: :w)
```

A propriedade `type`, podemos passar `:txt`para arquivos do tipo texto, ou `:bin` para arquivos do tipo binário.

```python
import file.*

my_file := read('some_file.txt', type: :txt)
```



