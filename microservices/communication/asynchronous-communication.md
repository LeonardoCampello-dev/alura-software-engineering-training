# Comunicação assíncrona

A comunicação síncrona é a mais comum, ela é indicada para muitos casos, mas ela tem problemas, e esses problemas normalmente podem ser resolvidos com comunicação assíncrona.

> Comunicação indireta

Existem cenários onde a resposta não precisar ser imediatamente obtida.

## Como se comunicar

- CQRS (background tasks)
- Eventos (mensageria)

## Exemplo simples

Ao realizar uma compra:

- Dados precisam ser validados
- Pagamento deve ser processado
  - Somente depois dos dados serem validados
- Estoque deve ser preparado
  - Pode ocorrer ao mesmo tempo que o pagamento é processado
- Logística deve ser iniciada
