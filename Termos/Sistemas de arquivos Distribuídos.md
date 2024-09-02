
## Hierarquia de um sistema distribuído 
![[HSD.png]]

## Vantagens e Desvantagens 

**Vantagens**:

- Escalabilidade: Pose ser dimensionado facilmente para lidar com cargas crescentes 
	- escalabilidade vertical: Mudança do hardware;
	- escalabilidade horizontal: Mudança para processo distribuído (maquinas adicionais) .
- Confiabilidade: Em caso de falha as outras máquinas iram continuar funcionando 
- Desempenho: As tarefas podem ser divididas assim concluídas em paralelo 

**Desvantagens**:

- Complexidade: de projetar e manter exigindo conhecimento especializado (separar as camadas os hardwares, implantar a solução e manter)
 - Sobrecarga: para máquinas precisam comunicar sobrecarga e latência 
 - Riscos de segurança: podem ser mais vulneráveis a ameaças
 - Custo: configurara e manter pode ser mais caro do que usar um único computador
## Exemplos
**Sistemas de arquivo distribuído**
- Hadoop
- Windows Distributed file system
- Network file sytem
- Server message block
- Google file system
- Lustre
- GlusterFS
- Amazon S3, Google cloud storage, Microsoft Block store

**Sistemas de processamento distribuído**

Pode ser usado sempre que for necessário algum tipo de computação e que o processamento local não seja suficiente. Quando é necessário alta capacidade computacional e/ou trabalhar com alto volume de dados

**Exemplos de sistemas de processamento**
- Spark
- Storm
- Snowflake
- AWS Glue
- AWS Athena
- Airflow
- DBT

