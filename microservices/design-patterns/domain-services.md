# Serviços de Domínio

Nós vamos pegar um pequeno domínio da nossa aplicação e separar em um serviço.

- Domain-driven Design
  - É interessante que para construir serviços de domínio, nós tenhamos conhecimento ou uma certa conciência do que é DDD. Através das práticas de DDD temos um domínio bem definido no nosso sistema.
- Comece modelando seu domínio, não pensando na persistência
  - Ex: Temos um serviço de Aluno (Alura), sempre que um aluno se matricular, nós vamos precisar consumir um domínio que lida especificamente com aluno. Esse serviço de aluno vai ter todas as regras relacionadas com a entidade.
- Avalie ações que serão disponibilizadas
  - Ex: Eu vou poder matricular um aluno através desse domínio? Ou vou simplesmente inserir um aluno? A matricula pode envolver coisas além de um aluno.
- Construa o serviço, pensando em primeiro no contrato
- REST e RPC podem andar juntos
  - REST é simplesmente representação de recursos e RPC envolve chamada de ações/funcionalidades, inclusive existe um padrão para isso, chamado Action Pattern.
