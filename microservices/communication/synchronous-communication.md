# Comunicação síncrona

## Comunicação direta

Diversos cenários nos obrigam a realizar "chamadas" e esperar por suas respostas.

Isso é o que conhecemos como comunicação síncrona.

## Como se comunicar

- HTTP
- gRPC
- Protocolos personalizados (ex: utilizando socket)

## Problema da abordagem

Ao realizar uma chamada direta para outro serviço e esperar sua resposta, problemas neste outro serviço nos afetarão diretamente.
