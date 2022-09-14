# Cuidando do host

Cuidar do host é basicamente como vamos lidar com os servidores (os componentes dos microsserviços).

## Onde manter cada componente de um microsserviço

Já vimos que cada microsserviço pode ter mais de um componente. Onde podemos manter todo esse sistema de forma que facilite tanto o desenvolvimento quanto o deploy?

## Máquinas virtuais (VMs)

O uso de máquinas virtuais foi e ainda é muito comum. Podemos provisionar uma VM de forma automatizada e integrar várias VMs.

O custo de processamento é alto. Dificilmente um computador de desenvolvimento rodará tranquilamente dezenas de VMs.

> Abordagem não interessente para microsserviços, custo muito alto.

## Sistemas em cloud

Sistemas de computação em nuvem estão cada vez mais famosos. Manter um ambiente de produção é relativamente simples hoje em dia.

Porém como ter um ambiente de desenvolvimento simplificado? Precisamos contratar uma máquina para cada dev?

> Abordagem não interessente para microsserviços, custo muito alto.

## Containers (Docker)

Essa é hoje a opção mais recomendada. Um ambiente de desenvolvimento é facilmente criado usando containers e diversos serviços de cloud possuem "container hosts", ou seja, ambientes próprios para "subirmos" containers.

> Abordagem mais interessante, consumo de recursos menor, facilidade de configuração e performance.
