# CNPJ MySQL

[![License](https://img.shields.io/badge/license-MIT-green.svg)](https://opensource.org/licenses/MIT)


# Iniciando os containers
```docker compose up -d```

## Baixando os arquivos
```docker compose exec pythonapp python dados_cnpj_baixa.py```

## Incluindo no banco de dados
```docker compose exec pythonapp python dados_cnpj_postgres.py```
