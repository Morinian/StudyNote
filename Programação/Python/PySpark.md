```python
df.limit(10) # ele apenas planeja
.explain() # mostrar qual o processo que ele montou - com true ele dá o plano logico

.show() # criado para linha de comando do cmd
.display() # leva a organização da tabela databricks
.count() # contagem
.printSchema() # Traz os tipos de cada coluna
f.expr # cria uma expressão
f.col # ele vetoriza
.cast(StringType()) 


groupBy() # faz um agrupamento
parceiro .igg() #  permite que atribue funções
```
append() **é útil para adicionar elementos a uma lista existente**

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

 ```python

df.gourpBy("coluna1","colunas2").count()

df_estoque = spark.read.parquet("s3a://your-bucket-name/path/to/file.csv")


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