# Lidando com logs

## Agregação de logs

- Formatos de log DEVEM ser compartilhados entre os serviços
- Uma taxonomia comum deve ser compartilhada
  - Ex: o que é um log de erro?
- Logs de monolitos são agregados por padrão. Com microsserviços o buraco é mais embaixo
- Parte da tarefa de agregação pode ser o parsing dos logs para categorizar corretamente

## Rastreando chamadas

- Uma parte importante de realizar logs é rastrear chamadas de uma execução
- Devemos poder reconstruir uma operação a partir de um identificador
- Isso é equivalente à _call stack_ de um sistema monolito
- Use padrões de _trace ID_ para gerar os logs
- Use ferramentas de gerenciamento (APMS) para visualizar
