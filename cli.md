---
description: Kymera possui sua própria CLI que ajuda a realizar diversas tarefas.
---

# CLI

## Criando Projeto

```bash
$ kym create <project_name>
```

Com `--type` ou `-t` poderá especificar o tipo de projeto:

* **cli** - Para linha de comando \(padrão\);
* **desktop** - Para aplicações desktop;
* **web** - Para aplicações web com o padrão MVC;
* **api** - Para aplicações web API;
* **micro** - Para aplicações web API voltadas para micro serviços.

```bash
$ kym create <project_name> -t  <cli | desktop | web | api | micro>
```

## Gerenciando Dependências

### Instalando Dependência

Adicionando dependência local:

```bash
$ kym add <package>
```

Adicionando dependência local para ambiente de desenvolvimento:

```bash
$ kym add --dev <package>
```

```bash
$ kym add -d <package>
```

Adicionando dependência local para ambiente de teste:

```bash
$ kym add --test <package>
```

```bash
$ kym add -t <package>
```

Instala todas as dependências _deps.yml_:

```bash
$ kym install
```

Adicionando dependência global:

```bash
$ kym global add <package>
```

### Removendo Dependência

Remove dependência local:

```bash
$ kym remove <package>
```

Remove dependência local em ambiente de desenvolvimento:

```bash
$ kym remove --dev <package>
```

```bash
$ kym remove -d <package>
```

Remove dependência local em ambiente de teste:

```bash
$ kym remove --test <package>
```

```bash
$ kym remove -t <package>
```

Remove dependência global:

```bash
$ kym global remove <package>
```

### Atualizar Dependência

Atualiza todas as dependências locais:

```bash
$ kym update
```

Atualiza dependência local específica:

```bash
$ kym update <package>
```

Atualiza todas as dependências locais de desenvolvimento:

```bash
$ kym update --dev
```

```bash
$ kym update -d
```

Atualiza dependência local de desenvolvimento específica:

```bash
$ kym update --dev <package>
```

```bash
$ kym update -d <package>
```

Atualiza todas as dependências locais de teste:

```bash
$ kym update --test
```

```bash
$ kym update -t
```

Atualiza dependência local de teste específica:

```bash
$ kym update --test <package>
```

```bash
$ kym update -t <package>
```

Atualiza todas as dependências globais:

```bash
$ kym global update
```

Atualiza dependência global específica:

```bash
$ kym global update <package>
```

### Execução

Para executar um projeto:

```bash
$ kym run
```

Para executar um arquivo específico:

```bash
$ kym run <nome_arquivo>.kym
```

Para executar em modo de debug, adicione `--debug` ou `-d`:

```bash
$ kym run -d
```

Para abrir o modo interativo passe `--interactive` ou `-i`:

```bash
$ kym -i
```

### Compilação

Para fazer o build de um projeto:

```bash
$ kym build
```

Para fazer o build de um arquivo:

```bash
$ kym build <arquivo>
```

