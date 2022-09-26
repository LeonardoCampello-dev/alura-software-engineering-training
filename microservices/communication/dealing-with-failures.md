# Lidando com falhas

_Como diz a lei de Murphy..._

Microsserviços possuem operações intensas em rede. As probabilidades de falha são grandes.

## Falhas em comunicação síncrona

- Circuit breaker
  - Pode ser um proxy que fica entre serviços, para não chamar um serviço diretamente. Quando esse proxy receber uma requisição, repassar para o serviço e na volta obter uma resposta de erro, na próxima requisição ele não vai repassar para o serviço. Assim evita que esse servidor com falha seja sobrecarregado de erros ou algo do tipo.
- Cache
  - Podemos utilizar cache para o usuário continuar recebendo respostas mesmo quando um servidor cair, obviamente isso não é aplicável em todos os casos, mas pode ser útil em alguns.

## Falhas em comunicação assíncrona

- Simples Retry
  - Tentar entregar mensagem novamente
- Retry com back-off
  - Tentou entrar uma mensagem, ela não foi recebida, espera um tempo e tenta novamente
- Fila de mensagens mortas
- Mensagens devem poder ser lidas fora de ordem
- Mensagens devem poder ser recebidas repetidamente (idempotência)
  - Se você executar uma coisa várias vezes, o resultado deve ser sempre o mesmo
