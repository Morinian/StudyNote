Repositório de dados unificado para armazenar grandes quantidades de informação com fontes variadas dentro de uma organização
- Várias fontes
- Grandes quantidades

	Verdade de dados: componente central de BI e relatórios. 

Ele é projetado para dar suporte a tomadas de decisão baseadas em dados e fornecer insights valiosos para impulsionar estratégias de negócios.
Banco de dados projetado especificamente para consultas e análises eficientes de grandes quantidades de dados de várias fontes, é um conceito com sql/nosql no formato [[Armazenamento#Colunar x Linha]].

![[DataWereHouse.png]]

Extract, transform and Load : [[Processo de ETL X ELT]] (extrai, transformar e carregar)

Benefícios:
- Melhora a padronização, qualidade e consistência dos dados
- Fornece inteligência de negócios aprimorada
- Aumenta o poder e a velocidade das cargas de trabalho de análise de dados e BI
- melhora o processo geral de tomada de decisão

- Dados estruturados e limpos facilita a analise e geração de relatórios
- Performance de consultar e relatórios é geralmente melhor devido a otimização de dos dados
- Governança de dados mais robusta
- Maior capacidade de suportar demandar

Desvantagens:
- Falta de flexibilidade de dados 
- Altos custos de implementação e manutenção regular

- Complexo de implementar e manter
- Exige um processo de limpeza e modelagem de dados rigoroso
- Restringe a capacidade de armazenar grande volumes de dados não estruturados 
- Pode ser limitado em lidar com dados em tempo real ou com fontes dinâmicas e não estruturadas 

## Quando usar um DW

Mais amplamente usada no [[armazenamento]] de dados projetado para consultas e análises de grandes quantidades de dados.

- Grande volume de dados
- Necessidade de desempenho e consulta analítica
- Necessidade de integrar dados de várias fontes
- Necessidade de oferecer suporte á inteligência de negócio
- Necessidade de dados históricos

## Como implementar?

1. Identificar os requisitos
2. Projeto e Arquitetura
3. Integração - ETL
4. Construir o DW
5. Carga de dados
6. Agendar atualizações
7. Acesso e Segurança
8. Monitoramento
9. Usar Data Marts - DW departamentais em geral com volume de dados menor
10. Manutenção do modelo de dados