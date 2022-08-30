# Um ou mais DBs?

## Single service database

- Problema: Escalabilidade do serviço e do banco são fortemente relacionados
- Solução: Cada serviço (que precisar) terá seu próprio banco de dados

## Shared service database

- Problema: Às vezes precisamos centralizar os dados (até por motivos contratuais)
- Solução: Trate esse banco em cada serviço como se ele fosse separado
