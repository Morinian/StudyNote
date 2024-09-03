
> [!info] Sobre
> Repositório centralizado projetado para armazenar - processar - proteger  grandes quantidades de dados **estruturados, semiestruturados e não estruturados**.
> 
> Permite armazenamento dos dados no seu formato bruto -> carrega, depois limpa e organiza, se não houver uma boa governança o datalake vira um problema e um risco.

Projetado para lidar com ampla variedade de tipos de dados, no caso tendo mais invista o banco de dados NoSql ou armazenamento distribuido 

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
Em geral, um Data Lake é uma boa opção se você tiver grandes volumes de dados estruturados e não estruturados que precisa armazenar e processar em escala ou se precisar de um repositório centralizado para armazenar e processar dados de várias fontes.
# Quando usar DL

Existe vários motivos
- Necessidade de armazenar e processar dados em sua forma bruta
- Necessidade de armazenar e processar grandes volumes de dados
- Necessidade de armazenar e processar dados estruturados e não estruturados
- Necessidade de escalabilidade
- Necessidade de um repositório de dados centralizado

## Como implementar?
1. Identificar os Requisitos
2. Escolher uma plataforma
3. Integração - ELT
4. Armazenamento
5. Agendamentos - configurar as atualizações 
6. Acesso - fornecer acesso aos dados do DL
7. Governança de Dados
8. Monitoramento