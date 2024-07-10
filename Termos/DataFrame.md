## O que é um DF

Objetos/tabela **bidimensionais**, de tamanho variável, semelhante a uma planilha do Excel, onde os dados são organizados em linhas e colunas. 

O seu formato é de uma **tabela**, onde os dados são organizados em linhas e colunas. 

Cada coluna pode conter diferentes tipos de dados, como números, strings, datas ou até mesmo objetos complexos.

Uma maneira comum de criar um DataFrame é a partir de um dicionário de listas. Cada chave do dicionário representa o nome de uma coluna e cada lista representa os valores dessa coluna.

```python

 Dados dos alunos dados = [ Row(Nome='João', Idade=20, Nota=8.5), 
 Row(Nome='Maria', Idade=18, Nota=9.2), 
 Row(Nome='Pedro', Idade=22, Nota=7.8) ] 
 
 # Criar o DataFrame a partir dos dados 
 df = spark.createDataFrame(dados) 
 
# Mostrar o DataFrame 
df.show()

# Parar a sessão Spark após o uso 
spark.stop()
```