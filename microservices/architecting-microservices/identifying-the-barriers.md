# Identificando barreiras

_Não existe regra para identificar barreiras, cada caso, é um caso._

- Uma abordagem muito útil para resolver este problema é utilizar o método **"monolith first"**. Quando você cria uma nova aplicação, você começa com uma abordagem monolítica, uma única aplicação, conforme a complexidade for aumentando você vai identificar os módulos de cada parte dessa aplicação e transformar em microsserviços. Ex: Se você tem um módulo que faz todo o gerenciamento de carrinho de forma desacoplada do resto da aplicação, este módulo pode facilmente virar um microsserviço.

- DDD pode ajudar muito na identificação de barreiras. Bounded contexts podem virar microsserviços.

## O que evitar?

Uma prática comum é transformar todos os "substantivos" do sistema em microsserviços, mas isso pode gerar muitos data services e serviços anêmicos demais.

## Pense antes de implementar

Desenhe um fluxo real usando uma arquitetura de microsserviços. Desta forma os problemas de cada abordagem surgirão.
