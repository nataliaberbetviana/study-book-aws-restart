<a id="top"></a>
# Arquitetura em Nuvem na AWS
Esse estudo analisa a estrutura de uma aplicação web simples, focando na interconexão entre os serviços essenciais da AWS para processar e armazenar dados de usuários. A arquitetura  demonstra como a nuvem abstrai a infraestrutura física e a transforma em serviços gerenciáveis e escaláveis.

---
## Estrutura Central: A Nuvem AWS
No centro da arquitetura está a **AWS Cloud**, que é a infraestrutura global da Amazon. Dentro dela, o primeiro passo é criar a **Nuvem Virtual Privada (VPC)**.
* **Nuvem AWS (AWS Cloud):** É a infraestrutura de servidores, redes e data centers da Amazon, disponível em todo o mundo. É o ambiente onde todos os serviços e recursos são executados.
* **Nuvem Virtual Privada (VPC):** É uma rede virtual isolada e segura que você cria dentro da nuvem da AWS. É como ter seu próprio data center privado, mas virtualmente. Todos os seus recursos são lançados e operam dentro dessa VP.

---
## Camada de Computação e Interação com o Usuário
O ponto de entrada da aplicação é a camada de computação, responsável por processar as requisições dos usuários e executar o código da aplicação.
* **Usuários:** A interação começa com os usuários, que acessam a aplicação através da internet.
* **Amazon EC2 (Elastic Compute Cloud):** A requisição do usuário chega a uma instância do EC2. que é um servidor virtual que executa seu código de aplicação. É a principal unidade de computação desta arquitetura, e está localizada dentro da sua VPC para garantir segurança.

---
## Camada de Dados e Armazenamento
Para ser funcional, a aplicação precisa de locais para armazenar dados dinâmicos e arquivos estáticos. A arquitetura separa esses dois tipos de armazenamento para otimizar desempenho e custo.
* **Amazon DynamoDB:** A aplicação em execução na instância EC2 se conecta so DynamoDB para salvar e recuperar dados. O **DynamoDB** é um serviço de banco de dados NoSQL totalmente gerenciado, ideal para dados que exigem alta performance e escalabilidade, como perfis de usuários, carrinhos de comprar ou sessões.
* **Amazon S3 (Simple Storage Service):** Se a aplicação precisa armazenar arquivos , como imagens ou vídeos, ela utiliza o S3. Esse serviço é um "balde" virtual para armazenamento de objetos, conhecido por sua alta durabilidade e baixo custo. O S3 é usado para dados não estruturados e é acessado de forma independente do banco de dados principal.
---
## **Conclusão**
Essa arquitetura simples ilustra a eficiência da nuvem. Em vez de gerenciar servidores físicos, redes e hardware de armazenamento, o desenvolvedor usa serviços gerenciados da AWS. Essa abordagem permite focar no código da aplicação, enquanto a AWS cuida da infraestrutura subjacente, do banco de dados e do armazenamento de arquivos, tudo de forma segura e escalável dentro de uma rede virtual isolada (VPC).


<div align="right">
  <a href="#top">
    <img src="https://img.shields.io/badge/-Voltar%20ao%20Topo-lightgrey?style=for-the-badge" alt="Botão de voltar ao topo">
  </a>
</div>