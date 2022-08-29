# Serviços de negócio

Frequentemente precisamos efetuar ações que demandam mais de um domínio, para esse caso utilizamos serviços de negócio.

Um serviço de negócio é basicamente a junção de vários domain services.

Ex: A matricula de um aluno não envolve apenas inserir um aluno no serviço de alunos, pode ser necessário registrar um aluno no serviço financeiro, no serviço de gamificação (Alura) também.

## Processo do domínio do negócio

- Proveem uma funcionalidade do negócio de mais alto nível (Matrícula)
- Permite encapsular domínios relacionados.

## Criando um serviço de negócio

- Identifique o processo que você pretende expor
  - Ex: Matricular aluno
- Identifique os domínios que serão necessários nesse serviço
  - Aluno
  - Matrícula financeira
  - Jogador
- Defina a API que será utilizada, focando no domínio e não nos dados
  - Não preciso ter detalhes de como o banco de dados está organizado
- Consuma serviços de domínio para executar os processos
