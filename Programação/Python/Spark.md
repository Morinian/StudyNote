O [[Spark]] surgiu como um projeto de pesquisa - 2009
"Spark: [[Cluster]] Computing With Working Sets"
	Matei Zahara

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

