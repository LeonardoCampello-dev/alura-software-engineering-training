# Segurança na rede

## Nem só de programação vive uma aplicação

É de extrema importância que façamos o uso de recursos de rede para manter nossa aplicação ainda mais segura.

## Redes virtuais

Imagine que temos 3 serviços e somente eles precisam se comunicar, não precisam de comunicação externa, nesse caso podemos colocar eles dentro de uma rede virtual, dessa forma, qualquer coisa que estiver fora dessa rede não vai chegar nos microsserviços.

## Sistemas de firewall

E se algum cliente precisar de comunicação externa, o que podemos fazer? Não vamos permitir o acesso direto, vamos utilizar um API Gateway e nele podemos ter ferramentas de Firewall. Ferramentas profissionais de Firewall podem previnir SQL injections, DoS e DDoS.

Utilizando um ponto de entrada nós aumentamos a segurança de rede dos nossos serviços.
