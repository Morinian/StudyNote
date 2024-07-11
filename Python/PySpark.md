O [[Spark]] surgiu como um projeto de pesquisa - 2009
"Spark: [[Cluster]] Computing With Working Sets"
	Matei Zahara

```ad-info
title: Execução

O Spark pode ser executado sozinho ou em vários gerenciadores de Cluster existentes. Atualmente oferece várias opções de implantação

Sua capacidade de processamento em memoria utilizando caxamento em memória que otimiza 

Ele lê dados do custer que cada etaparequer uma leitura
```

Processamento de dados estruturados e não estruturados

ELE SURGE APARTIR DE DA IDEA DA Hadoop - CRIADO APARTID DE AMBIENTES DISTRIBUIDOS 
esse drive consegue fazer a distribuição 
Hadoop ele faz todas as operações de escrita no hd - lendo e escrevendo
Spark (opensource) na memória RAM todos os passos que o Hadoop faz ele faz lendo a memória RAM comportamento laser (PREGUIÇOSO)

tranformations ela não faz nada lea programa a execução 
action - ele vai fazer a cadeia que programou 

tranformation ele analisa o meta dados - planejamento
df.limit(10) - ele apenas planeja
.explain() - mostrar quyal o processo que ele montou - com true ele dá o plano logico

.show() = criado para linha de comando do cmd
.display() = leva a organização da tabela databricks
.count()
.printSchema() = vai trazer os tipos
f.expr = cria uma expressão
f.col = ele vetoriza
.cast(StringType())=
tabelas databricks = tabela parquet file

groupBy() = faz um agrupamento
parceiro .igg()´= permite que atribue funções
row_num 

window functioon

parquet = arquivo otimizado  ele é um arquivo inteligente ele pega os dados da tabela (deoende do motor row layout) pode salvo de 2 formas layout de coluna ou linha
ele inditifica as loculnas e separa por grupos todas as linhas 

 Contar quantos ambiente por usuários  

``` python
 display(
	 df_user
	 .select(
		 "nm_user",
		 "ds_email",
		 f.lower(f.col("nm_user)).alias("select_lower_nm_user"),
		 #dá pra fazer muita coisa no select
		 "ds_env"
	 )
	 .filter("nm_user ilike 'felipe%") 
	 # aspas duplas = sql | ilike = insensitive
	 
	 .filter(f.col(nm_user).ilike("felipe%")) #col vetoriza a coluna
	 .withColumn("lower_nm_user",f.expr("lower(nm_user)")) 
	 
	 .withColumn("full_nm_user",
	 f.expr("CASE WHEN nm_user = 'Feipe solares' THEN 'Felipe Solares da Silva' ELSE nm_user END") 

	 .withColumn("python_full_nm_user",f.when(f.col("nm_user" == "Felipe Solares", "Felipe Solares da Silva")).otherwise(f.col("nm_user")))
 )
 ```

 
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