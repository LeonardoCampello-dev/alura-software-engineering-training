# O que são Microsserviços?

## Aplicações monolíticas

Em uma aplicação monolítica todas as regras de negócio e todo código estarão nela. No caso de um aplicação de loja, todas regras de negócio relacionadas com produtos, pedidos e pagamento estariam na mesma aplicação e provavelmente esses produtos, pedidos e pagamentos estão na mesma base de dados.

### Alguns problemas

- Demoras no deploy
- Falhas podem derrubar o sistema todo
- Um projeto = Uma stack de tecnologias

## Arquitetura de microsserviços

Arquitetura de microsserviços é uma forma de organizar a aplicação onde cada parte do nosso sistema é um serviço independente.

Em uma aplicação de loja, quando você faz uma requisição, provavelmente ira bater em um ponto central, e esse ponto central irá definir qual serviço precisa ser utilizado para atender a requisição, por exemplo, uma requisição para um serviço de catálogo, neste serviço vão existir apenas produtos, não vai existir nada relacionado com pedidos ou pagamento. Por exemplo, se meu sistema de pedidos estiver fora do ar, não terei nenhum problema com meu sistema de catálogo.

### Definição formal

Microsserviços são uma abordagem arquitetônica e organizacional do desenvolvimento de software na qual o software consiste em pequenos serviços independentes que se comunicam usando APIs bem definidas. Esses serviços pertencem a pequenas equipes autossuficientes.

### Algumas vantagens

- Projetos independentes = tecnologias independentes
- Falha em um serviço é isolada
- Deploys menores e mais rápidos

### Algumas desvantagens

- Maior complexidade no desenvolvimento e infra
- Debug mais complexo
- Comunicação entre serviços deve ser bem pensada
- Diversas tecnologias podem ser um problema
- Monitoramento é crucial e mais complexo

## Quando utilizar microsserviços

Uma abordagem bem interessante é a de Martin Fowler, que é basicamente tomar monolítos como padrão, começar com aplicações monolíticas e conforme os módulos forem se tornando muito grandes ou receberem um volume muito alto de requisições, você vai migrando para microsserviços.

[_Referência Martin Fowler_](https://martinfowler.com/bliki/MonolithFirst.html)
