# CNPJ MySQL

[![License](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT)
![Docker](https://img.shields.io/badge/-Docker-2496ED?logo=docker&logoColor=white)

## O que é o projeto original do CNPJ MySQL?

São script's em python para carregar os arquivos de cnpj dos dados públicos da Receita Federal em MYSQL e POSTGRESQL. 
O código é compatível com o layout das tabelas disponibilizadas pela Receita Federal a partir de 2021.

## O que foi alterado em relação ao original?

- **Dockerização**: Todo o projeto foi dockerizado para facilitar a implantação e execução. Isso significa que você não precisa se preocupar em configurar o ambiente manualmente. Basta ter o Docker instalado e você estará pronto para rodar a aplicação.

- **Docker Compose**: Foi criado um arquivo `docker-compose.yml` que define como os diferentes serviços interagem entre si. Com um único comando, você pode iniciar todos os contêineres necessários, incluindo a aplicação Python e o banco de dados PostgreSQL.

## Pré-requisitos

- Docker em ambiente linux

---

# Como utilizar?

## Iniciando os containers
```docker compose up -d```

## Baixando os arquivos
```docker compose exec pythonapp python dados_cnpj_baixa.py```

## Incluindo no banco de dados
```docker compose exec pythonapp python dados_cnpj_postgres.py```
