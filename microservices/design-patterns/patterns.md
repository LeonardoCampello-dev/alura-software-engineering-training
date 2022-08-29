## Strangler pattern

- Quebrar um monolito, tirando as funcionalidades dele
- Podemos começar isolando os dados
  - Podemos começar a migração para microsserviços separando o banco de dados. Para sincronizar os novos bancos de dados podemos fazer algum ajuste de infraestrutura ou algum ajuste diretamente no monolito.
- Ou podemos começar isolando o domínio
  - Podemos começar separando os domínios e continuar se conectando no mesmo banco de dados.

## Sidecar pattern

Podemos ter uma lógica igual em diversos serviços e queremos compartilhar esse código, porém não queremos criar um serviço para isso. Às vezes ter serviços demais pode ser um problema.

- Determine um processo comum
  - Ex: Realizar logs
- Construa um módulo compartilhável
  - Ex: Se utilizamos node, podemos criar um pacote NPM.
- Aplique esse _sidecar_ nos serviços que precisam dele
