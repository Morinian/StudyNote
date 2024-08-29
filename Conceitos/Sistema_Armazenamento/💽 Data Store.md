 # O que é
 
É um repositório para armazenar e gerenciar dados, dividindo em 7 categorias 
1. Banco de dados Relacional ([[Armazenamento#SQL]] -normalmente usado em DWs)
2. Banco de dados não Relacional [[Armazenamento#NoSQL]]] - Podem ser usados em DWs ou Data Lakes)
	- Entram na categoria de Data Store:
		1. [[Armazenamento#Armazenamento de arquivos]] (Distribuídos ou não, são usados em DL e Data lakehouse)
		2. Armazenamento de Key-value
			- Outra maneira de armazenar dados não relacionais é o de chave valor 
			- Hashmap em escala de produção: Redis
		3. Full-text Search engine
			- Mecanismo de pesquisa de texto
			- Tipo especial para pesquisar documentos de texto
			- Envia documento semiestruturados para o mecanismo de pesquisa
			- Elasticsearch é o principal representante 
		1. Fila de mensagens 
		2. In-memory Data store
