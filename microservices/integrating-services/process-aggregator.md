# Agregando processos

## Process aggregator pattern

- Serviços de negócio agregam serviços de domínio
- _Process aggregators_ agregam serviços de negócio
- Agregadores fazem as chamadas para os serviços necessários e montam a resposta correta
- Pode (e deve) ter lógica de processamento

## Construindo um agregador

- Defina um novo modelo para representar os dados agregados
- A partir deste modelo, pense na API que fornecerá as operações
