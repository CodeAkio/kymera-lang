---
description: Kimera possui sua própria CLI que ajuda a realizar diversas tarefas.
---

# CLI

## Criando Projeto

```bash
$ kim new <project_name>
```

Com `--type` ou `-t` poderá especificar o tipo de projeto:

* **cli** - Para linha de comando (padrão);
* **desktop** - Para aplicações desktop;
* **web** - Para aplicações web com o padrão MVC;
* **api** - Para aplicações web API;
* **micro** - Para aplicações web API voltadas para micro serviços.

```bash
$ kim new <project_name> -t  <cli | desktop | web | api | micro>
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
$ kim add <package>
```

Adicionando dependência local para ambiente de desenvolvimento:

```bash
$ kim add --dev <package>
```

```bash
$ kim add -d <package>
```

Adicionando dependência local para ambiente de teste:

```bash
$ kim add --test <package>
```

```bash
$ kim add -t <package>
```

Instala todas as dependências _deps.yml_:

```bash
$ kim install
```

Adicionando dependência global:

```bash
$ kim global add <package>
```

### Removendo Dependência

Remove dependência local:

```bash
$ kim remove <package>
```

Remove dependência local em ambiente de desenvolvimento:

```bash
$ kim remove --dev <package>
```

```bash
$ kim remove -d <package>
```

Remove dependência local em ambiente de teste:

```bash
$ kim remove --test <package>
```

```bash
$ kim remove -t <package>
```

Remove dependência global:

```bash
$ kim global remove <package>
```

### Atualizar Dependência

Atualiza todas as dependências locais:

```bash
$ kim update
```

Atualiza dependência local específica:

```bash
$ kim update <package>
```

Atualiza todas as dependências locais de desenvolvimento:

```bash
$ kim update --dev
```

```bash
$ kim update -d
```

Atualiza dependência local de desenvolvimento específica:

```bash
$ kim update --dev <package>
```

```bash
$ kim update -d <package>
```

Atualiza todas as dependências locais de teste:

```bash
$ kim update --test
```

```bash
$ kim update -t
```

Atualiza dependência local de teste específica:

```bash
$ kim update --test <package>
```

```bash
$ kim update -t <package>
```

Atualiza todas as dependências globais:

```bash
$ kim global update
```

Atualiza dependência global específica:

```bash
$ kim global update <package>
```

## Execução

Para executar um projeto:

```bash
$ kim run
```

Para executar um arquivo específico:

```bash
$ kim run <nome_arquivo.kim>
```

Para executar em modo de debug, adicione `--debug` ou `-d`:

```bash
$ kim run -d
```

Para abrir o modo interativo passe `--interactive` ou `-i`:

```bash
$ kim -i
```

## Compilação

Para fazer o build de um projeto:

```bash
$ kim build
```

Para fazer o build de um arquivo:

```bash
$ kim build <arquivo.kim>
```

## Checagem

Existem ferramentas de checagem de código.

{% hint style="info" %}
Se um arquivo não for especificado ele faz com o projeto
{% endhint %}

Faz checagem de erros no código:

```bash
$ kim check --error [arquivo.kim]
```

Faz checagem de formatação, convenções de código e boas práticas, mas não as corrige, apenas alerta o que deve ser feito:

```bash
$ kim check --format [arquivo.kim]
```

Faz checagem de vulnerabilidades relacionadas a pacotes ou versão do projeto:

```
$ kim check --sec [arquivo.kim]
```

Faz checagem de atualizações disponíveis relacionadas a pacotes ou versão do projeto:

```bash
$ kim check --update [arquivo.kim]
```

