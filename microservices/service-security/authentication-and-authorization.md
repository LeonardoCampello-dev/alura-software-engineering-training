# Autenticação e autorização

São conceitos utilizados em qualquer sistema, mas quando trabalhamos com microsserviços, precisamos ter um cuidado maior com isso.

## Não devemos confiar em ninguém

Ter uma certa segurança (amplamente falando) não isenta nossa aplicação de lidar diretamente com esse assunto.

## Autenticação

Cada requisição deve informar quem é o cliente. A partir dessa informação, nossa aplicação pode decidir se a operação será realizada ou não.

## Técnicas de autenticação

- Basic HTTP
  - Consiste em todas requisições enviar um user e password em um cabeçalho HTTP, porém isso exige que o cliente armazene user e password, isso pode ser inseguro.
- Tokens (JWT)
- OAuth
  - Autenticação com o Google, GitHub e etc
  - Delega responsabilidade para alguém maior
- OpenID Connect

## Autenticação vs Autorização

A **autenticação** nos permite saber quem está realizando determinada chamada.

A partir do processo de **autorização** decidiremos se a pessoa autenticada pode realizar tal ação.

## Técnicas de autorização

- ACL (Access control list)
- RBAC (Role-based access control)
- On behalf of
