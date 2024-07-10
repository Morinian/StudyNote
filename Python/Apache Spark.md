O Spark surgiu como um projeto de pesquisa - 2009
"Spark: [[Cluster]] Computing With Working Sets"
	Matei Zahara

```ad-info
title: Execução

O Spark pode ser executado sozinho ou em vários gerenciadores de Cluster existentes. Atualmente oferece várias opções de implantação

Sua capacidade de processamento em memoria utilizando caxamento em memória que otimiza 

Ele lê dados do custer que cada etaparequer uma leitura
```

Processamento de dados estruturados e não estruturados

## Iniciando Codificação
-------------------------------
	Versão completa do código está no meu notebook [PySpark](https://colab.research.google.com/drive/1dHjCre8JO661GDpxApJUZJQ1LNjEw6w1?authuser=1#scrollTo=uTYaZorZCZm3)

Iniciando a Sessão do Spark para utilização

```python
spark = (
    SparkSession.builder
    .master("local") #Trabalha com cluster
    .appName("Estudo") #nome da nossa seção
    .getOrCreate() #Puxa sessão recente se não ele cria
)
```

Criando [[DataFrame]]
```python
df = spark.read.csv('Dados/wc2018-players.csv', header=True, inferSchema=True) 
#df = apenas uma variavel
#ler aquivo csv
#heade = true cabeçalho normalmente existe
#inferSchema define o tipo se não deixar true ele deixa tudo como String
```