
![[ciclovidaengenharia.png]]


# Fonte de Dados

# Processo de dados 

Ingestão de dados: visa tirar os dados da fonte e fazer a ingestão na sua plataforma de dados (DataLake, Nuvem, S3 etc), dependendo da fonte terá que ver os conectores e merges.

Transformação e enriquecimento: em geral parte complexa, tendo limpeza organização e transformação, ==colocar dados em contexto== 

Carga e uso dos dados: Preciso fazer algo com os dados já enriquecidos, podemos armazenar para depois utilizar, já utilizar ou os dois. Normalmente etapa mais simples já que é mais sobre tomada de decisão para o uso dos dados.

Armazenamento: Dados precisam residir em algum local, pode ser um [[💽Data Lake]], [[💽Data LakeHouse]] ou entre outras opções.

# Etapas 
## Arquitetura de dados

Com base nos requerimento o arquiteto desenha a solução o engenheiro vai incrementar a arquitetura

Arquitetura não é estático : ela vai mudar conforme o processo é construído, novos produtos , tecnologias tudo pode mudar tendo que remanejar 

## Gestão de Dados e Metadados 

Não posso autorizar qualquer pessoa acessar os dados
Quem são os donos dos dados ? - gestão de dados
Meta dados pode ser usados para analise -> onde dado passa e se origina 

## Orquestração 

Eu posso ter uma pipeline cada cada tarefa e assim precisamos gerenciar e assim surge orquestração .
Concatenar pipelines entra nessa seção 

## Segurança

Configuração de alta disponibilidade (segurança está configurada?)
Contrato de segurança e LGBD

## CI/CD

Nasceu no desenvolvimento de software - onde fala que precisa ser atualizado de forma constante com segurança 
DevOps

## DataOps

Segmentação na área de dados 
Olhar para todo o ciclo de vida, ajudar a monitorar e gerenciar todo esse processo