Repositório centralizado projetado para armazenar - processar - proteger  grandes quantidades de dados **estruturados, semiestruturados e não estruturados**.

Utilizando uma arquitetura plana, tendo grande informações avançadas não estruturadas

Estruturado com base no S3 e Unity Catalog do Databricks.

![[DataLake.png]]

	O S3 irá sustentar todo o armazenamento dos dados ainda no seu formato nativo e não estruturado - temporário ou permanente - presentes nas camadas transient e raw. Já o catálogo de dados no databricks, sustentará os dados estruturados e semiestruturados, sendo auto gerenciadas e manipuladas em formato de Delta Table.

# Camadas/Zonas do Data Lake

![[DataLakeZone.png]]
### Transient Zone

Zona transitória, na qual os dados serão ingeridos pelo Data Lake. É a porta de **entrada do dado bruto**, tende a ser uma camada de repouso. Ideal é a vida útil desse dado não seja longa.

Depois que os dados ingeridos forem alocados na Raw, os arquivos aqui são excluídos.

### Raw Data Zone

Um dos  principais diferenciais de um Data Lake.
Camada dos **dados brutos**, [[As-is]], sem nenhum tratamento e mantendo o tipo do dado original.

Podendo armazenar com agilidade todos os dados de fonte relevantes, agregando valor por ser uma fonte crua.

### Trusted Zone

Utilizada para tratamento e enriquecimento dos dados. Padronização de data types, limpeza de dados, mascaramento, conversão para formato otimizado de dados. 
Para serem consumidos e já possuem garantias de [Data Quality](https://medium.com/datalakers-blog/como-garantir-a-qualidade-dos-dados-5668d06516c), podendo ser considerados **exatos e confiáveis**.

### Refined Zone

Onde são aplicadas regras de negócio, geradas visões e conjuntos de dados a serem consumidos por outros sistemas.

