# Event-Driven Architecture

Basicamente vamos modelar nossa arquitetura de uma forma diferente, para que nossos componentes sendo microsserviços ou o que forem, se comuniquem de uma forma diferente do que estamos habituados, ou seja, requisições HTTP.

## Modelo de requisições

Normalmente utilizamos o modelo de requisições.

Ex: Temos um cliente que faz uma requisição para adicionar um item no carrinho, o serviço de carrinho faz uma requisição para o serviço de pedido, o serviço de pedido precisa se comunicar com o serviço de catálogo que talvez precise se comunicar com algum outro serviço. Imagine se um erro ocorrer no final dessa cadeia de requisições, vamos ter todo nosso fluxo com erro. A ideia de ter uma arquitetura orientada a eventos é desacoplar toda essa comunicação.

## Centralizando a comunicação

Nós vamos centralizar a comunicação em algum tipo de serviço e esse serviço distribui tudo que for necessário.

Ex: Temos um cliente que faz uma requisição para um serviço de carrinho (adicionar um item), esse serviço vai enviar um evento para o centralizador de eventos, o centralizador de eventos vai receber o evento do carrinho e encaminhar para o serviço de pedido, o serviço de pedido vai criar um novo evento que vai ser enviado para o serviço de catálogo e esse serviço de catálogo pode também gerar um evento, no final disso tudo é gerado um evento para informar ao nosso serviço de carrinho que está tudo certo.

Durante toda essas comunicações o serviço de carrinho poderia liberar o cliente para fazer outras coisas ou ficar esperando uma mensagem de todos eventos finalizados.

A principal vantagem de centralizar a comunicação é a facilitação da escabilidade horizontal, pois podemos ter um serviço completamente independente dos outros. Dessa forma conseguimos escalar melhor é garantir que nossos sistemas lidem melhor com cenários de falha.

### Centralizados de eventos (Event Bus)

Normalmente nosso centralizador de evento é implementado por serviços de mensageria, como RabbitMQ, Azure Service Bus e AWS SQS.
