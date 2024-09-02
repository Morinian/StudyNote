- Processamento de Dados 
- Controle
- Movimentação de Dados
- Armazenamento de dados

## Cloud
- Não focar no futuro e sim no agora
- Manter cloud pode ser pior que comprar uma maquina

# Memória

## Localização 
- Interna
- Externa
## Capacidade
- Numero de bytes
- Numero de palavras
## Método de acesso 
- Sequencial : leitura em linha reta ==fita==
- Aleatório: mesmo tempo de resposta
- Associativa: o dado está em outro lugar
- Direto: Precisa rodas a fila (rua) inteira para achar - não consegue contabilizar o tempo de resposta ==CD, HD== - Nero (imperador que queimou Roma) usado para gravar CD 
## Desemprenho
- Tempo de acesso e ciclo
- Taxa de transferência 
## Tipo físico
- semicondutor
- magnético
- Optico 
## Características físicas
- Volátil: Tirar da tomada perdi tudo
- Não volátil apagável ou não : Manter energia logo salva os dados
## Organização
- Modulo de memorias

# Visão geral

Quanto mais barato -> mais espaço
Quanto mais caro -> mais velocidade

registrado | velocidada
registrador -> Velocidade altíssima 
CPU Cache -> do lado do processador-> Alta
RAM -> fora do processador -> média
memórias secundarias -> Baixa

## Endereçamento 

**Direto**: acessa valor diretamente
**Indireto**: ponteiro (podemos mandar alterar diretamente para main sem precisar dar return)

## Localização 

**Interna** : Acessível direto pelo processado | Memoria RAM, Cache e registradores
**Externa** : Acessível pelo processador | Cloud, HD, SDD, Pendrive

## Memória interna
==Não volátil: não se perde ao deixar sem energia==

### ROM (Somente leitura) 
É a memória que controla os componentes da placa mãe, gravada diretamente da fábrica  - BIOS 

## PROM 
Passa para de gravar na fábrica e ser programável

## EPROM
Apagável a nível chip

## EEPROM/ FLASH (Memory-pendrive)
Apagável a nível de byte e gravada eletronicamente
Podendo atualizar 


# Erros em memória

Causas: falhas permanentes | Falhas não permanentes
==Matemático criou um jeito de validar aquilo que foi salvo==

Algoritmo de Hamming (1 bit de erro)
Validar para não ter erro de armazenamento

palavra 1 byte -> código de validação (sai uma chave e armazena isso e o numero) -> célula de memória -> código de validação -> comparador

Ele faz o mesmo calculo podendo corrigir ele 
par : 0
impar: 1

se a chave for incorreta com a do começo analisa a interseção e muda o valor 

# Dispositivos E/S

**Humano** : Construído para a comunicação com o usuário

**Maquina** : Construído para comunicação com o equipamento

## Técnicas

E/S Programada: Dados trocados entre o processador e o modulo, processador espera até que o processo termine; Só faz o segundo pedido quando o outro lado executou.

	E/S Controlada por interrupção: Dados trocados entre o processador e o modulo, interrompe o processador ao terminar o processo.

Acesso direto a memória DMA: é capaz de imitar o processador assumindo o controle do barramento do sistema, rouba o ciclo que não estão em uso.























