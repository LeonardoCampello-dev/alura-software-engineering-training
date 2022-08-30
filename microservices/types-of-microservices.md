# Tipos de microsserviços

## Data service

É um dos tipos de serviço mais comuns, esse tipo de serviço que fornece acesso direto a determinada fonte de dados.

## Business service

Um business service normalmente é um aglomerado de data services, porém, ele não só expõe acesso a dados, ele tem regras por trás disso.

## Translation service

Frequentemente precisamos acessar APIs externas, para isso, podemos utilizar um serviço de tradução, esse tipo de serviço basicamente permite uma entrada de dados a partir do nosso sistema e envia uma requisição para um sistema externo, como um serviço de pagamentos.

## Edge service

Edge também é um padrão de projeto de microsserviços, esse tipo de serviço permite nós permite expor um tipo de serviço para cada cliente.

Ex: Você pode estar acessando uma aula da Alura pelo browser ou pelo app mobile, no app talvez eu não precise de alguns dados que são informados no browser. Então, a partir do app mobile, você pode estar acessando um Edge service que faz somente as requisições necessárias para assistir uma aula no app.
