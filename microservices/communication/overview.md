# Como lidar com a comunicação entre serviços?

- Todo serviço pode se comunicar (diretamente) com qualquer outro?
- O front-end deve chamar os serviços diretamente?

_Regras: Não há regras_

## Possíveis problemas em uma comunicação direta entre microsserviços

- Dependências descontroladas
  - Dificuldade de atualização
  - Quebra o princípio de microsserviços serem independentes
- Falhas em cascata
  - A aplicação inteira pode cair por causa de uma falha isolada
- Performance prejudicada
  - Uma falha pode demorar para ser retornada, o que pode causar problema de performance
