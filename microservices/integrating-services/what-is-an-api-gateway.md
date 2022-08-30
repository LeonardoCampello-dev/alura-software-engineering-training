# O que é um API Gateway?

Ponto único de entrada

Imagine um cenário onde temos vários microsserviços, com várias URLs diferentes ou IPs, acessar todos esses serviços é uma tarefa um pouco difícil. Então para centralizar o acesso a vários serviços, podemos utilizar um API Gateway.

## API Gateway

<p align="center">
  <img src="https://www.tibco.com/sites/tibco/files/media_entity/2020-05/api-gateway-diagram.svg" width="400">
</p>

A ideia por trás desse componente que adicionamos na nossa estrutura de microsserviços é centralizar o acesso aos nossos serviços. Imagine que temos uma requisição vindo de um browser, mobile ou até por um desenvolvedor utilizando algum tipo de ferramenta, todas essas requisições serão enviadas para um único ponto de entrada, o API Gateway.

- Problema que o API Gateway visa resolver: Clientes acessando livremente os serviços geram caos
- Solução: Gateway fornece um proxy, uma fachada, para as necessidades reais
- **Desvantagem de utilizar um Gateway: Esse portão de entrada pode se tornar um ponto central de falha**

## Comportamentos do Gateway

Um gateway pode ter vários comportamentos, o básico seria fazer o roteamento, mas ele também pode fazer o load balancing, logs de tudo que está entrando nas nossas aplicações, pode informar ao cliente como cada URL deve ser armazenada em cache e pode até realizar autenticação utilizando algum serviço externo.
