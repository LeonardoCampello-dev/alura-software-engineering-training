# Modelagem de Eventos

### Definição formal

"Event Modeling is a method of describing systems using an example of how information has changed within them over time."

## Fases

1. Brainstorming

"We have someone explain the goals of the project and other information. The participants then envision what system would look and behave like. They put down all the events that they can conceive of having happened. Here we gently introduce the concept that only state-changing events are to be specified. Often, people will name guest viewed calendar for room availability. We put those aside for now - they are not events."

Fase onde você reúne todas equipes técnicas e não técnicas e todo mundo vai descrever os eventos que pensam.

_Ex: Reserva de hotel_

- Uma pessoa se registrou no sistema
- Uma pessoa reservou um quarto
- O quarto foi higienizado para ser habitado
- O pagamento foi requisitado
- Etc.

Nós apenas precisamos mapear os eventos que alteram o estado da nossa aplicação, por exemplo, uma pessoa apenas olhar um quarto não altera o estado da aplicação.

No final do Brainstorming teremos uma pilha de ideias desorganizadas.

2. Ordenação lógica (the plot)

"Now the task is to create a plausible story made of these events. So they are arranged in a line and everyone reviews this time line to understand that this makes sense as events that happen in order."

Nesta etapa devemos organizar todos os eventos em uma linha que faça sentido para contar uma história.

3. Storyboard

"Next, the wireframes or mockups of the story are needed to address those are visual learners. More importantly, each field must be represented so that the blueprint for the system has the source of and destination of the information represented from the user's perspective."

Na terceira etapa vamos criar interfaces de como esses eventos vão acontecer, isso ajuda as pessoas que são mais visuais a entender como cada evento acontece. E a partir disto podemos identificar mais de uma tela que linda com o mesmo evento e etc.

4. Identificando entradas

"From the earlier section we saw that we need to show how we enable the user to change the state of the system. This is usually the step in which we do this introduction of these blue boxes. Each time an event is stored due to a users action, we link that to the UI by a command that shows what we are getting from the screen or implicity from client state if it's a web application."

Na quarta etapa nós identificamos o que cada tela vai ter de entrada para modificar o estado do nosso sistema.

5. Identificando saídas

"Again looking back at our goals for the blueprint, we now have to link information accumulated by storing events back into the UI via views. These may be like the calendar view in our hotel system that will show the availability of rooms when a user is looking to book a room."

Na quinta etapa fazemos o inverso da etapa anterior, vamos identificar as saídas de cada evento.

6. Lei de conway

"Now that we know how information gets in and out of our system, we can start to look at organizing the events themselves into swimlanes. We need to do this to allow the system to exist as a set of autonomous parts that separate teams can own. This allows specialization to happen to a level that we control instead of falling out of the composition of teams."

Basicamente essa lei diz que quando uma empresa desenvolve um sistema e automatiza um processo, ela vai inevitavelmente seguir uma estrutura no sistema semelhante com a estrutura da empresa.

Neste momento vamos separar os eventos em raias onde cada uma dessas raias pode ser referente a um departamento da empresa ou equipe de desenvolvimento.

7. Elaboração de cenários

"Each workflow step is tied to either a command or a view/read-model. How we make them is still collaboratively with all participants in the same space. A Give-When-Then can be constructed one after the other very rapidly while being reviewed by multiple role representatives."

Nesta etapa final nós vamos elaborar de fato cada cenário, se esse necessário precisa de entradas, como vamos pegar as entradas e etc.

## Supostas vantagens

A principal vantagem é que de acordo com a passagem do tempo a complexidade de adição de novas funcionalidades não vai aumentar, pois um fluxo de uma história não afeta o fluxo de outra história.
