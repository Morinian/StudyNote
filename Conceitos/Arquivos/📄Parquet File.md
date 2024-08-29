
## O que é o Parquet?

É um formato de arquivo de dados em colunas de código aberto projetado para armazenamento e recuperação de dados eficientes

```ad-info
title: Projeção
collapse: none

O parquet foi projetado para ser um formato semelhante a RCFile e ORC, outros formatos de arquivo de armazenamento no Hadoop
```

Parquet é como a tabela que usamos no DW

Não é a única opção para armazenar dados de forma eficiente

A ferramenta de código aberto chamada Delta Lake, popularizada pela Databricks, usa arquivos no formato parquet para fornecer muitos de seus recursos ao criar um [[💽Data LakeHouse]] , por exemplo.
### Casos específicos
- Armazenamento de grandes quantidades de dados estruturados e semiestruturados
- Consulta de dados usando ferramentas semelhantes a SQL
	- Apache Spark
- Compartilhamento de dados entre sistemas
### Características

- Formato de arquivo de código aberto sem custo
- Aceita qualquer linguagem
- Formato baseado em colunas
- Usado para casos de uso analíticos
- Fácil de particionar (excelente para leitura dos dados)

### Benefícios do Parquet

- Ótimo para armazenar big data
- Economize armazenamento em nuvem 
- Taxa de transferência e desemprenho de dados aprimorados