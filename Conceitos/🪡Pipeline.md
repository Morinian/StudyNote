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

É amplo é processo envolvido no transporte de dados a um local para outro incluindo limpeza transformação enriquecimento segurança orquestração integração/entrega continuo (CI/CD)

Pode ser composto de vários pipelines ETL além de tarefas complementares como enriquecimento de dados, gestão de metadados, linhagem de dados.

### Características pipeline de dados

As principais características ao considerar um pipeline de dados incluem:

- Processamento de dados contínuo e extensível.
- A elasticidade e agilidade da nuvem.
- Recursos isolados e independentes para processamento de dados.
- Acesso democratizado a dados e gerenciamento de autoatendimento.
- Alta disponibilidade e recuperação de desastres