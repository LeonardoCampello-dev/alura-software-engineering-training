# O que é Mensageria?

### Definição formal

Mensageria é um conceito que define que sistemas distribuídos possam se comunicar por meio de troca de mensagens (evento), sendo estas mensagens "gerenciadas" por um Message Broker (servidor/módulo de mensagens).

O conceito de mensageria que faz uso de algum software é a ideia que dois sistemas diferentes vão se comunicar através de trocas de mensagem. Uma requisição HTTP também é uma troca de mensagem, porém esse tipo de troca de mensagem é um pouco diferente, pois funciona de forma assíncrona.

**Ex:** Temos um sistema A e um sistema B, e eles precisam se comunicar, só que o sistema A não precisa esperar a resposta do sistema B pra continuar funcionando, supondo que queira enviar um e-mail, só é necessário avisar ao sistema que queremos enviar um e-mail, nós não queremos ficar esperando o sistema avisar que enviou o e-mail ou algo do tipo, se por algum motivo ocorrer um erro ao enviar o e-mail, o sistema avisa depois. Então esse sistema A vai adicionar ao Message Broker um evento (mensagem) dizendo que quer enviar um e-mail e nesse evento terão informações, como conteúdo e destinatário do e-mail.

### Conceito Pub/Sub

Esse é um conceito onde temos dois papéis, o de publisher quem publica um evento e o de subscriber quem vai consumir essa mensagem.

<p align="center">
  <img src="https://dashbird.io/wp-content/uploads/2021/01/pub-sub-messaging.png" width="500" />
</p>
