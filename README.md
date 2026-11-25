# B3 Market Data Pipeline

## Sobre o projeto

O **B3 Market Data Pipeline** é um projeto prático de Engenharia de Dados desenvolvido no contexto de uma pós-graduação em Engenharia de Dados.

O objetivo é construir um pipeline de ingestão de dados financeiros da Bolsa de Valores Brasileira (B3), utilizando a API Alpha Vantage como fonte de dados, Databricks como ambiente de desenvolvimento e processamento com Apache Spark e PySpark.

O projeto contempla a extração de cotações de ações, preparação dos dados, armazenamento utilizando Delta Lake e consultas analíticas com Spark SQL.

## Objetivos

- Implementar a ingestão de dados financeiros por meio de uma API REST.
- Desenvolver processos de extração e transformação utilizando Python e PySpark.
- Trabalhar com DataFrames e processamento distribuído.
- Implementar armazenamento de dados no formato Delta Lake.
- Aplicar conceitos da arquitetura Medallion, iniciando pela camada Bronze.
- Desenvolver consultas e análises utilizando Spark SQL.
- Aplicar boas práticas de organização, versionamento e documentação de projetos de Engenharia de Dados.

## Tecnologias utilizadas

| Tecnologia | Finalidade |
|---|---|
| Databricks Free Edition | Ambiente de desenvolvimento |
| Python | Linguagem de programação |
| Apache Spark | Processamento de dados |
| PySpark | Manipulação de dados com Spark |
| Pandas | Preparação e tratamento inicial |
| Requests | Consumo da API REST |
| Alpha Vantage API | Fonte de dados financeiros |
| Delta Lake | Armazenamento e gerenciamento dos dados |
| Spark SQL | Consultas e análises |
| Git e GitHub | Versionamento e documentação |

## Fonte de dados

**Alpha Vantage API**

A API fornece dados financeiros e séries históricas de cotações.

Ativos inicialmente considerados:

- PETR4 — Petrobras
- VALE3 — Vale
- ITUB4 — Itaú Unibanco
- BBDC4 — Bradesco
- ABEV3 — Ambev

## Estrutura do projeto

```text
b3-market-data-pipeline/
│
├── README.md
├── config
├── api
└── viewdata
```

### Notebooks

**config**

Centraliza os parâmetros do projeto, lista de ativos, configurações de acesso à API e caminhos de armazenamento.

**api**

Responsável pelo consumo da Alpha Vantage API, ingestão, preparação dos dados e persistência no Delta Lake.

**viewdata**

Responsável pela leitura dos dados armazenados, consultas com Spark SQL e visualizações.

## Arquitetura inicial

O projeto inicia com a camada Bronze da arquitetura Medallion, armazenando os dados provenientes da API no formato Delta Lake.

Fluxo proposto:

1. Extração dos dados da Alpha Vantage API.
2. Preparação e conversão dos dados para Spark DataFrame.
3. Armazenamento na camada Bronze utilizando Delta Lake.
4. Consulta e visualização utilizando Spark SQL.

## Evolução do projeto

O desenvolvimento será incremental, contemplando inicialmente a ingestão e persistência dos dados na camada Bronze.

Como evolução, estão previstos estudos e implementações de qualidade de dados, cargas incrementais, prevenção de duplicidades e expansão para as camadas Silver e Gold.

## Ambiente de desenvolvimento

- Plataforma: Databricks Free Edition.
- Linguagem principal: Python.
- Framework de processamento: Apache Spark / PySpark.
- Controle de versão: Git / GitHub.

## Finalidade

Projeto acadêmico e prático voltado ao desenvolvimento de conhecimentos em Engenharia de Dados, processamento distribuído, integração de APIs e armazenamento de dados utilizando tecnologias do ecossistema Databricks.