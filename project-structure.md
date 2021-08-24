---
description: Os projetos possuem uma estrutura básica de pastas e arquivos.
---

# Project Structure

Todos os arquivos do projeto, ficam dentro de uma **pasta** com o mesmo **nome do projeto** em **snake\_case**.

```text
project_name/
|-- .build/
|-- config/
|---- config.kym
|---- dev.kym
|---- prod.kym
|---- stage.kym
|---- test.kym
|-- docs/
|---- main.yml
|-- src/
|---- main.kym
|-- tests/
|---- main_test.kyms
|-- deps.yml
|-- deps.lock
|-- LICENSE.md
|-- README.md
|-- .editorconfig
|-- .env
|-- .gitignore
```

Os arquivos do Kymera possuem duas extensões:

* **.kym** - Ele é compilado para binário;
* **.kyms** - Ele é apenas interpretado.

A pasta **.build/** é onde fica os arquivos compilados, prontos para produção;

A pasta **config/** é onde ficam as configurações da aplicação:

* **config.kym** - É onde ficam as configurações gerais que servem para todo o ambiente, nele ficam configurações como nome do projeto, versão, banco de dados, etc.
* **dev.kym** - São as configurações específicas para ambiente de desenvolvimento;
* **prod.kym** - São as configurações específicas para ambiente de produção;
* **stage.kym** - São as configurações específicas para ambiente de staging;
* **test.kym** - São as configurações específicas para ambiente de teste;

A pasta **docs/** mantém toda a documentação do projeto.

A pasta **src/** é onde vai residir o nosso código fonte.

* O **src/main.kym** é o _entrypoint_ da aplicação.

A pasta **test/** é onde ficam todos os nossos testes da aplicação e os arquivos possuem a extensão **.kyms**;

O arquivo **deps.yml** é onde ficam todas as dependências do projeto, separado por ambiente;

O arquivo **deps.lock** é o arquivo que registra a versão exata e o hash do pacote que instalou, isso evita que ocorra erros de versão;

O **.env** é um arquivo que armazena as variáveis de ambiente.

