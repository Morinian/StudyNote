## O que é?

De forma resumida, um pipeline de dados, é responsável por executar uma série de scripts de forma ordenada, estabelecida no momento de sua criação, a fim de realizar a operação de [[Processo de ETL X ELT]] (Extract, Transform, Load), ou seja, extrair, processar e armazenar um conjunto de dados para que possa ser consumido pelos analistas de dados e cientistas de dados.

Pipeline é um passo a passo, é a representação de um processo que está dividido em fases para colocar a aplicação em produção. Como fazer a build do código, executar testes automatizados e a implantação em ambientes de teste e de produção

```ad-note

Pipeline é um conceito e pode ser implementador de muitas formas diferentes desde ferramentas de automação em ambientes local, ferramentas de nuvem ou em programação.
```


Pipeline é um meio de mover dados de uma origem para um destino (DW/DL). Ao longo do caminho os dados são transformados e otimizados chegando a um estado em que podem ser analisar e usados para desenvolver insights de negócios.

Conjunto das etapas envolvidas na agregação e movimentação de dados automatizando muitas das etapas manuseias envolvidas na transformação e otimização do carregamento de dados
## Componentes

- Origem dos dados
Importantíssima a forma que extraímos e como fazemos isso podendo causar lentidões na origem
- Processamento 
Mais complexa e extensa 
- Destino
Não precisa armazenar os dados no destino

## Pipeline de dados

É amplo é processo envolvido no transporte de dados a um local para outro incluindo limpeza transformação enriquecimento segurança orquestração integração/entrega continuo [[CI & CD]]

Pode ser composto de vários pipelines ETL além de tarefas complementares como enriquecimento de dados, gestão de metadados, linhagem de dados.

São parte da arquitetura de dados de uma empresa é parte da plataforma de dados da empresa.

### Características pipeline de dados

As principais características ao considerar um pipeline de dados incluem:

- Processamento de dados contínuo e extensível.
- A elasticidade e agilidade da nuvem.
- Recursos isolados e independentes para processamento de dados.
- Acesso democratizado a dados e gerenciamento de autoatendimento.
- Alta disponibilidade e recuperação de desastres

# Arquitetura Pipeline de dados

Iniciamos uma pipeline de dados pela compreensão dos requisitos de negócio e o que se espera do uso de dados no dia a dia.

Deve ter um propósito e deve fazer parte da arquitetura de dados, uma boa estratégia é criar uma PoC (Prova de conceito) uma espécie de laboratório, que simula cenários 

## Tipos de pipeline
### Pipeline de Machine learning

É todo o ecossistema, desde os usuários de negócio até as previsões em tempo real, as linhas de produção

Hoje em dia não é tarefa de um profissional, é normalmente muito segmentado assim cada profissional em cada etapa
### Pipeline de Dados

Pedaço da pipeline de machine learning

Pipeline ETL é um pedaço de pipeline de dados, ou seja em um pipeline de dados podemos ter várias pipelines especificas (dependendo da arquitetura)

Extração de dados -> Limpeza e transformação -> Processamento dos Dados -> Fluxo de dados

### Pipeline ETL

Pedacinho de um pipeline de dados

Extração de dados -> Limpeza e transformação 

# Perguntas para arquitetura

## Inicialmente 

- Quais os requisitos do negócio (Inicial do projeto)
- Quais resultados finais são necessários (Final do projeto)
- Os dados estão disponíveis? Quais são as fontes?
- Quais formatos dos dados disponíveis
- Qual crescimento esperado do volume de dados?
- Quanto de armazenamento é necessário?
- Quanto de capacidade computacional será necessário?
- Usaremos dados em batch, em streaming ou ambos?
- Já temos tecnologia que permita criar os pipelines?
- Quais tecnologias devem ser consideradas?
- Quais são os acordos de nível de serviço (SLA's) - tempo mínimo (entrega, execução etc) 
- Custo de implementar e manter os pipelines?
- Qual será o destino do pipeline? - pode ser outro pipeline
- Como será o monitoramento?
- Usaremos diversos pipelines encadeados?
- Vamos criar os pipelines locais, na nuvem ou ambos?