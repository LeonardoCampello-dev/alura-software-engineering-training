# Contratos de microsserviços

> Microsserviços são independentes

Um microsserviço expõe alguma forma de comunicação (uma API). Isso é o contrato entre este microsserviço e seus clientes.

_Mas como manter minha API sempre a mesma se meu projeto precisa de atualizações e novas funcionalidades?_

## Microsserviços são independentes

- Apenas faça modificações aditivas
  - Novos endpoints
  - Novos campos (opcionais) em cada recurso
  - Nunca modificar uma funcionalidade existente
  - Nunca remover uma funcionalidade
- Versionamento de APIs
  - Ao lançar uma v2, a v1 deve continuar funcionando, inalterada
  - Isso pode ser trabalhoso, porém é mais fácil para o cliente
  - Ex: Temos um endpoint de pedidos `/v1/orders`, se precisarmos mudar o contrato deste endpoint, não apenas fazer uma modificação aditiva, neste caso vamos criar um novo endpoint `/v2/orders`. Porém a v1 precisa continuar existindo e funcionando da mesma forma.
- Manter equipes separadas, donas de cada serviço
  - A mesma equipe não vai alterar os clientes
  - Para adicionar funcionalidades que dependem de outros, solicitações formais podem ser feitas
