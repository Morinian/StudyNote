#### Conceito geral
O [[Spark]] surgiu como um projeto de pesquisa - 2009
"Spark: [[Cluster]] Computing With Working Sets"
	Matei Zahara

![[PandavsPyspark.png]]

O Apache Spark é uma engine de computação unificada e um conjunto de bibliotecas para processamento de dados paralelos em clusters de computadores.

```ad-info
title: Execução

O Spark pode ser executado sozinho ou em vários gerenciadores de Cluster existentes. Atualmente oferece várias opções de implantação

Sua capacidade de processamento em memoria utilizando caxamento em memória que otimiza 

Ele lê dados do custer que cada etapa requer uma leitura
```

Processamento de dados estruturados e não estruturados.
Muito da popularidade do Spark se deve aos fatores listados abaixo:

- Suporta diferentes linguagens de programação como Java, Python, Scala e R.
- Possibilita streaming de dados em tempo real.
- É possível rodar em uma única máquina assim como em grandes clusters de computadores.
- Suporta SQL.
- Possui bibliotecas para criar aplicações com Machine Learning, MLlib.
- Realiza processamento de dados em grafos com GraphX.
- É uma ferramenta open-source.

O Spark tem diversos componentes para diferentes tipos de processamentos, todos construídos sobre o Spark Core, que é o componente que disponibiliza as funções básicas para o processamento como as funções map, reduce, filter e collect.

![[sparcore.png]]


### RDD (Resilient Distributed Dataset)

```ad-info
title: Origin

RDD foi a principal API voltada para o usuário no Spark desde seu início. Basicamente, um RDD é uma coleção distribuída imutável de elementos de seus dados, particionados entre nós em seu cluster que podem ser operados em paralelo com uma API de baixo nível que oferece transformações e ações.
```

As operações disponíveis nos RDDs e são essencialmente duas, ações e transformações.

![[actionTransfSpark.png]]

O componente do Spark responsável por mapear todas as ações e transformações em um programa é chamado de **Dag (Direct Acyclic Graph),** que está presente dentro do Driver Program, no diagrama de arquitetura do Spark.
O Dag também mapeia todas as tasks e stages necessárias para rodar o código.
### Arquitetura 

- **Driver program** - Orquestra a execução do processamento de dados
- **Cluster manager** - gerencias máquinas em um cluster (forma distribuída)
- **Workers nodes** - máquinas que executam as tarefas de um programa.
	- executado local : Driver Program e Workes (**Standalone**).
	- executado na mesma máquina onde o programa foi iniciado: **Cliente mode**
	- driver Program rode em qualquer máquina em um cluster: **modo Cluster**
	- Faz uma ponte entre driver Program e os executores: Spark Context 

Quando se faz um programa spark essa operação é traduzida para um plano de execução lógico, chamado de Lineage, que podia ser uma sequência como carregar os dados, aplicar um filtro e retornar o dados.

O spark cria um objeto chamado Dag Scheduler, que armazena a sequência presente no Lineage. Com essas informações, o Spark divide as tarefas entre os diferentes Workers para serem executadas.

![[arq_spark.png]]
### Hadoop x Spark

Ele surgiu a partir da ideia do Hadoop ==Criado a partir de ambientes distribuídos== esse drive consegue fazer a distribuição.

Hadoop ele faz todas as operações de escrita no HD - lendo e escrevendo
Spark (open-source) faz na memória - comportamento laser (PREGUIÇOSO) 

- Tranformations  - ela não faz nada, apenas lê a programa de execução, ele analisa o meta dados - planejamento 
- Action - ele vai fazer a cadeia que programou 

Por conta do Hadoop também ser um framework de processamento distribuído, é natural que exista comparações. Mas o Hadoop é composto por diversos componentes, entre eles o MapReduce, que é a ferramenta que desempenha processamento dados com o mesmo objetivo do Spark. A seguir um breve comparativo entre os dois:

Hadoop MapReduce:
- Armazena o resultado das operações parciais e finais em disco.
- Paradigma de desenvolvimento Map Reduce.

Apache Spark:
- Armazena o resultado das operações parciais em memória e finais em disco (esse último configurável).
- Paradigma de desenvolvimento Map Reduce entre outros

