## Extração, Transformação e Carregamento - ETL
 
 É um pipeline de dados usado para coletar dados de várias fontes. Em seguida, ele transforma os dados de acordo com as regras de negócio e os carrega em um armazenamento de dados de destino. O trabalho de transformação no ETL ocorre em um mecanismo especializado e, muitas vezes, envolve o uso de tabelas de preparo para armazenar os dados temporariamente enquanto eles são transformados e, por fim, carregados no destino.
 
![[etl.png]]
## Extração, Carregamento e Transformação - ELT

O ELT (extração, carregamento e transformação) difere do ETL somente no local em que ocorre a transformação. No pipeline de ELT, a transformação ocorre no armazenamento de dados de destino. Em vez de usar um mecanismo de transformação separado, as funcionalidades de processamento do armazenamento de dados de destino são usadas para transformar os dados. Isso simplifica a arquitetura pela remoção do mecanismo de transformação do pipeline. Outro benefício dessa abordagem é que o dimensionamento do armazenamento de dados de destino também dimensiona o desempenho do pipeline ELT. No entanto, o ELT só funciona bem quando o sistema de destino é poderoso o suficiente para transformar os dados com eficiência.

![[elt.png]]