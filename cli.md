---
description: Kymera possui sua própria CLI que ajuda a realizar diversas tarefas.
---

# CLI

## Criando Projeto

```bash
$ kym new <project_name>
```

Com `--type` ou `-t` poderá especificar o tipo de projeto:

* **cli** - Para linha de comando (padrão);
* **desktop** - Para aplicações desktop;
* **web** - Para aplicações web com o padrão MVC;
* **api** - Para aplicações web API;
* **micro** - Para aplicações web API voltadas para micro serviços.

```bash
$ kym new <project_name> -t  <cli | desktop | web | api | micro>
```

Cada tipo de projeto faz várias perguntas sobre o seu projeto e já tenta pré-configurar o ambiente, como:

* Versão do projeto;
* Github do projeto;
* Descrição do projeto;
* Banco de dados (PostgreSQL, Maria DB, MySQL, MS SQL Server, Redis, MongoDB);
* Cache;
* Autenticação (JWT, PIN, e-mail + senha, usuário + senha, Autenticação social, OAUTH 2, 2FA);
* Envio de e-mail (SMTP, Send Grid, Mailgun, Amazon SES, Mailchimp);
  * Template de e-mail (Bootstrap E-mail, MJML, Foundation for Emails);
* Hospedagem (AWS, Google App Engine, Azure, Heroku, Digital Ocean);
* Docker;
* LESS, SASS ou SCSS;
* Sistema de CI/CD;
* Framework CSS (Bootstrap, Bulma, Material Design);

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

## Execução

Para executar um projeto:

```bash
$ kym run
```

Para executar um arquivo específico:

```bash
$ kym run <nome_arquivo.kym>
```

Para executar em modo de debug, adicione `--debug` ou `-d`:

```bash
$ kym run -d
```

Para abrir o modo interativo passe `--interactive` ou `-i`:

```bash
$ kym -i
```

## Compilação

Para fazer o build de um projeto:

```bash
$ kym build
```

Para fazer o build de um arquivo:

```bash
$ kym build <arquivo.kym>
```

## Checagem

Existem ferramentas de checagem de código.

{% hint style="info" %}
Se um arquivo não for especificado ele faz com o projeto
{% endhint %}

Faz checagem de erros no código:

```bash
$ kym check --error [arquivo.kym]
```

Faz checagem de formatação, convenções de código e boas práticas, mas não as corrige, apenas alerta o que deve ser feito:

```bash
$ kym check --format [arquivo.kym]
```

Faz checagem de vulnerabilidades relacionadas a pacotes ou versão do projeto:

```
$ kym check --sec [arquivo.kym]
```

Faz checagem de atualizações disponíveis relacionadas a pacotes ou versão do projeto:

```bash
$ kym check --update [arquivo.kym]
```

