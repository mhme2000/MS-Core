<h1 align="center">
   MS-Core
</h1>

## 💻 Sobre o projeto

MS-Core. Projeto agregador que compõe o serviço de eccomerce desenvolvido no trabalho de conclusão de curso da pós tech da FIAP. Todos os projetos possuem instruções de execução no seu próprio README, mas de forma sucinta, para orquestração dos containers de forma local, foi utilizado o docker-compose, já para a orquestração em nuvem, foi utilizado o Elastic Container Service da AWS e o RabbitMQ para comunicação assíncrona via mensageria.

Serviços que estão presentes nessa solução:

- [x] Monolito desenvolvido em NestJS [Legado], hoje serve apenas para base de conhecimento. Repositório : https://github.com/mhme2000/tech-challenge-grupo-15
- [x] MS Delivery, responsável pelo envio de e-mails. Repositório : https://github.com/mhme2000/MS-Delivery
- [x] MS-Payments, responsável pela geração e processamento de pagamentos. Repositório: https://github.com/mhme2000/MS-Payments
- [x] MS-Products, responsável pelo gerenciamento do catálogo de produtos. Repositório : https://github.com/mhme2000/MS-Products
- [x] MS-Customers, responsável pelo gerenciamento de clientes da plataforma. Repositório : https://github.com/mhme2000/MS-Customers
- [x] MS-Infrastructure, responsável por prover toda a infraestrutura dentro da aws através do terraform. Repositório : https://github.com/mhme2000/MS-Infrastructure
- [x] MS-Orders, responsável pelo gerenciamento do pedido, desde sua concepção até o estado de pronto. Repositório: https://github.com/gustavo-clemente/tech-challenge-ms-order
 
 Foi escolhido o padrão saga coreografado para ser aplicado nessa solução. O padrão Saga Coreografado é uma abordagem de design de software que visa coordenar e gerenciar transações distribuídas em sistemas distribuídos. Por ser uma solução com poucos microsserviços, a escolha parece nos atender muito bem. Além de coordenar as transações distribuídas, podemos ressaltar a garantia de consistência nas transações, a tolerância a falhas, a escalabilidade e a flexibilidade como principais vantagens.

---

## 💻 Desenho da arquitetura

Arquitetura geral na nuvem aws:

![image](https://github.com/mhme2000/MS-Core/assets/45264849/8c8ad3b3-d45e-49a3-88cd-7bfed33315d9)

Arquitetura detalhada da SAGA coreografada com RabbitMQ:

![image](https://github.com/mhme2000/MS-Core/assets/45264849/489ae671-e754-444b-b9a6-e6f44243a790)

