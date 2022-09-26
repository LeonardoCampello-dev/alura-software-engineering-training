# Service Discovery

Microsserviços podem estar na mesma rede ou em redes separadas, e cada serviço pode estar exposto por um IP.

Mas lidar diretamente com o IP de cada serviço pode trazer muitos problemas.

## DNS (Domain name system)

Algo que já fazemos na internet, podemos também fazer em redes privadas: registro de nomes.

DNS pode ser utilizado como service registry para sabermos como acessar cada serviço.

Um registro de serviço pode ter informações sobre quais processos ou máquinas estão de pé e sem falha.
