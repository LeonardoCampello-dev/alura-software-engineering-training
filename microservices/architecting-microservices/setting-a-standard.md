# Definindo um padrão

## Padronizando a criação

Diversas tarefas devem ser realizadas de forma semelhante entre os serviços:

- Criação de logs
  - Formato
  - Destino
- Verificação de status (health checks)
- Monitoramento de métricas
- Busca por configuração e secrets

## Templates ou exemplos

Podemos ter um projeto "esqueleto" com tudo que qualquer microsserviço precisa.

Scripts de build, mínimo código necessário, etc.

Isso nos dá muita agilidade, mas tira um pouco da flexibilidade.

## Containers

Uma ótima forma de ter uma espécie de "template" é tendo uma imagem base para containers que conterão microsserviços.

A partir da imagem, só precisamos começar a codificar e rodar códigos nos containers criados.
