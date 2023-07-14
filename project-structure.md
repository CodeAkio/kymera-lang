---
description: Os projetos possuem uma estrutura básica de pastas e arquivos.
---

# Project Structure

Todos os arquivos do projeto, ficam dentro de uma **pasta** com o mesmo **nome do projeto** em **snake\_case**.

```
project_name/
|-- .build/
|-- config/
|---- config.kim
|---- dev.kim
|---- prod.kim
|---- stage.kim
|---- test.kim
|-- docs/
|---- main.yml
|-- src/
|---- main.kim
|-- tests/
|---- unit/
|------ main_test.kims
|-- deps.yml
|-- deps.lock
|-- LICENSE.md
|-- README.md
|-- .editorconfig
|-- .env
|-- .gitignore
```

Os arquivos do Kim possuem duas extensões:

* **.kim** - Ele é compilado para binário;
* **.kims** - Ele é apenas interpretado.

A pasta **.build/** é onde fica os arquivos compilados, prontos para produção;

A pasta **config/** é onde ficam as configurações da aplicação:

* **config.kim** - É onde ficam as configurações gerais que servem para todo o ambiente, nele ficam configurações como nome do projeto, versão, banco de dados, etc.
* **dev.kim** - São as configurações específicas para ambiente de desenvolvimento;
* **prod.kim** - São as configurações específicas para ambiente de produção;
* **stage.kim** - São as configurações específicas para ambiente de staging;
* **test.kim** - São as configurações específicas para ambiente de teste;

A pasta **docs/** mantém toda a documentação do projeto.

A pasta **src/** é onde vai residir o nosso código fonte.

* O **src/main.kim** é o _entrypoint_ da aplicação.

A pasta **test/** é onde ficam todos os nossos testes da aplicação e os arquivos possuem a extensão **.kims**;

O arquivo **deps.yml** é onde ficam todas as dependências do projeto, separado por ambiente;

O arquivo **deps.lock** é o arquivo que registra a versão exata e o hash do pacote que instalou, isso evita que ocorra erros de versão;

O **.env** é um arquivo que armazena as variáveis de ambiente.
