# O que é arquitetura hexagonal?

<p align="center">
  <img src="https://miro.medium.com/max/1200/1*LF3qzk0dgk9kfnplYYKv4Q.png" width="500px" style="border-radius: 8px" />
</p>

## Arquitetura hexagonal (Ports and Adapters)

A ideia deste padrão arquitetural é isolar toda a regra de negócios (domínio) e todo o resto fica do lado externo. Toda a comunicação que não está diretamente relacionada ao domínio vai chegar por meio de alguma porta (primary). Essa porta vai enviar os dados e algum adaptador vai ler as informações que chegam por essa porta.

Essas informações vão precisar ser armazenadas em algum local, como um banco de dados, porém nossa aplicação (domínio) não vai conhecer este banco dados, nossa aplicação vai se comunicar por meio de uma porta de saída (secondary), nossa regra de negócios vai conhecer apenas interfaces de comunicação.

A arquitetura visa isolar a regra de negócio, porém não dita como deve ser feito, dentro da camada de regra de negócios você pode usar o padrão que preferir, como DDD ou algo do tipo.

Na arquitetura hexagonal temos dois tipos de adaptadores, os adaptadores primários são os que recebem dados e enviam para a regra de negócios, os adaptadores secundários são os que pegam dados das nossas regras de negócios e enviam para fora da aplicação.
