# Domain-Driven Design (Design de código orientado ao domínio)

## O que é? (definição formal)

Design orientado ao domínio é o conceito de que a estrutura e o idioma do seu código devem corresponder ao domínio comercial.

- O seu código deve refletir a realidade do negócio.

## Padrões estratégicos

- Linguagem Ubíqua (Onipresente)
  - Se eu tenho um conceito no meu domínio que eu chamo de Aluno, o meu código deve refletir isso, então eu tenho uma classe chamada Aluno.
- Contextos delimitados
  - Módulos maiores na nossa aplicação, **Ex:** na Alura temos o sistema acadêmico (para assistir aulas, avaliar instrutores e etc) e temos o sistema de ranking (onde ganhamos pontos por ações feitas na plataforma), dois contextos diferentes. O DDD incentiva a separar esses contextos, podendo ser até dois sistemas diferentes.
- Domínio e subdomínio
  - **Ex:** na Alura o domínio principal é o acadêmico, porém, para que esse conceito funcione ele precisa de subdomínios.

## Padrões táticos (blocos de construção)

- Entidades
- Repositórios
  - Fazem a tradução de entidades para a camada de persistência, utilizando interfaces parecidas com coleções.
- Eventos
  - Aluno criado, aluno atualizado e etc.
- Módulos
- Serviços
  - Algo que representa uma ação (regra acontecendo): marcar formação como concluída, assistir curso e etc.
