
# Por que o Armazenamento de Dados é importante?

- Onde os dados residem?
Os dados residem em arquivos que são armazenados no disco físico ou outras mídias de armazenamento de dados 

## Padrões de Acesso Definem o tipo de armazenamento 
## Diferença de [[📄Parquet File]] ou Avro
## Diferença do formato JSON ou CSV
## Diferença em HDF5 ou PICKLE
## Diferença de SQL / NoSQL ou armazenamento de arquivos

	Depende dos padrões de acesso.

## SQL : 
é o formato tradicional no formato tabular mais antigos e amplamente usados nos dias de hoje na qual é ideal para dados estruturados, usando SGBDs.
Se o padrão de acesso é muito frequente, acessando de formas diferentes os dados.

## NoSQL : 
nasceu na era do BigData para permitir o armazenamento de dados em diferentes formatos, dados semiestruturados no formato JSON,XML ou colunar.
Temos mais soluções em nosql na qual é orientado a performance e facilidade de uso

## Armazenamento de arquivos:
Assim tendo o ponto do V de variedade no BigData, em formatos adversos podem não ser ideias em foco na performance de acesso com diferentes formatos e sistemas. Armazenar em ambiente distribuído ou em um único computador 

- Podem ser local ou em redes (NTFS, FAT, NAS, SAN)
- Podem ser distribuídos (HDFS - Haddop Distributed File System, Object Storage)
- Podem ser na nuvem (Amazon S3, Azure Blob Storage, Google Storage, Delta Lake)
- O objetivo é armazenar dados em qualquer formato de arquivo (CSV, JSON, PARQUET, AVRO, ORC, etc)
- Baixo custo geralmente

# Colunar x Linha 

![[baseadoemlinha.png]]
Não é um formato pensado para performance, é fácil mas não ideal

![[baseadoemcoluna.png]]
001 índice que podemos fazer pesquisas, pode ser muito mais performático que em linha