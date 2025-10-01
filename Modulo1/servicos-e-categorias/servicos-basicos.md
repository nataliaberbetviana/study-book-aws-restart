<a id="top"></a>
# A Fundamentação: Infraestrutura e Serviços Básicos
A vasta gama de serviços da AWS é organizada em categorias para facilitar a vida de quem constrói na nuvem. Em vez de ser uma bagunça de produtos aleatórios, eles se encaixam em uma hierarquia lógica, permitindo que você escolha o nível de abstração que deseja - desde ter controle total sobre um servidor virtual até que apenas enviar seu código e deixar que a AWS gerencie tudo.

## A Fundamentação: Infraestrutura e Serviços Básicos
Esta camada é a base de tudo. Os serviços aqui fornecem os recursos brutos, como poder de processamento, armazenamento e redes. É onde você tem mais controle.
* **Serviços de Computação**
    * **Amazon EC2 (Elastic Compute Cloud):** Pense no EC2 como sua **máquina virtual** na nuvem. Ele é a opção mais flexível, onde você pode escolher o SO, instalar qualquer software e ter controle total sobre o ambiente. É a escolha ideal para quem está "levantando e transferindo" (lift-and-shift) uma aplicação de um data center local para a nuvem ou para quem precisa de um ambiente com configurações específicas. A cobrança é granular, geralmente por segundo.
    * **AWS Lambda:** O oposto do EC2 em termos de controle. O Lambda é a essência do modelo **serverless**. Em vez de gerenciar um servidor, você apenas faz o upload do seu código e o Lambda executa em resposta a eventos. Você **não paga por tempo ocioso**, apenas pelo tempo de execução do seu código, em incrementos de milissegundos. É perfeito para APIs, processamento de dados em tempo real e automação.
    * **AWS Elastic Beanstalk:** Se você quer focar apenas no código, mas sem abrir mão da flexibilidade, o Elastic Beanstalk é a resposta. Ele é um serviço de **Plataforma como Serviço (PaaS)** que automatiza o processo de implantação. Você apenas faz o upload do seu código e o Beanstalk provisiona automaticamente as instâncias EC2, os balanceadores de carga e o que mais for necessário, cuidando de toda a infraestrutura por trás.
* **Serviços de Armazenamento**
    * **Amazon S3 (Simple Storage Service):** O S3 é um serviço de **armazenamento de objetos**, ideal para dados não estruturados. Pense neles como um enorme balde virtual para guardar arquivos. Ele tem durabilidade e escalabilidade praticamente ilimitadas, e você paga apenas pelo volume de dados armazenados.
    * **Amazon EBS (Elastic Block Store):** O EBS é como um **disco rígido virtual** para suas instâncias EC2. Ele fornece volumes de armazenamento persistentes em nível de bloco que podem ser anexados a uma instância, ideal para o SO, bancos de dados e qualquer dado que precisa de acesso rápido e de baixa latência.
    * **Amazon EFS (Elastic File System):** Diferente do EBS, o EFS é um **sistema de arquivos de rede**. Isso significa que ele pode ser montado e acessado por múltiplas instâncias EC2 ao mesmo tempo. É a escolha perfeita para workloads que precisam de armazenamento compartilhado, como ambientes de desenvolvimento e aplicações que precisam de um repositório de arquivos comum.

---

## Serviços de Plataforma e Aplicação (Abstração Média)
Esta camada é onde a AWS assume o gerenciamento da infraestrutura subjacente para você, permitindo que você se encontre na lógica da sua aplicação.
* **Banco de Dados:**
    * **Amazon RDS (Relational Database Service):** Um serviço para **bancos de dados relacionais gerenciados**. O RDS automatiza tarefas complexas como instalação, backups, patches, escalabilidade e failover. Ele suporta motores de banco de dados populares, como MySQL, PostgreSQL, e Microsoft SQL Server, liberando você das tarefas de administração.
    * **Amazon DynamoDB:** Um serviço de **banco de dados NoSQL** totalmente gerenciado. Ele é projetado para aplicações que precisam de performance de alta escala com baixa latência, como jogos, adtech e sistemas e-commerce.
* **Contêineres**
    * **Amazon ECS (Elastic Container Service) & Amazon EKS (Elastic Kubernetes Service):** São serviços para **orquestração de contêineres**. Eles ajudam você a gerenciar grandes grupos de contêineres e a garantir que eles estejam sempre em execução. O EKS é uma versão gerenciada do Kubernetes, enquanto o ECS é a solução nativa da AWS.
    * **AWS Fargate:** O Fargate é o motor de computação **serverless para contêineres**. Ele elimina a necessidade de gerenciar instâncias EC2 onde os contêineres rodam, permitindo que você se concentre apenas em empacotar sua aplicação em um contêiner e executá-la.

---

## Serviços de Gerenciamento e Segurança
Esta categoria inclui as ferramentas que ajudam você a controlar, monitorar e proteger seu ambiente na nuvem.
* **AWS IAM (Identify and Accem Management):** O IAM é o pilar da **segurança**. Ele permite que você gerencie usuários, defina quem pode fazer o quê e em qual serviço, garantindo que o princípio do privilégio mínimo seja aplicado.
* **Amazon CloudWatch:** Uma ferramenta de **monitoramento e observabilidade** que coleta métricas e logs de todos os seus recursos AWS. Ele permite que você crie painéis de controle, defina alarmes e reaja a mudanças no desempenho.
* **AWS Config:** Um serviço para **auditoria** e **conformidade**. O Config grava o histórico de configurações de seus recursos, permitindo que você rastreie alterações e garanta que suas configurações estejam de acordo com as políticas da sua empresa.
* **AWS Cost Explorer & Budgets:** Ferramentas para **gerenciamento de custos**. O Cost Explorer ajuda a analisar e visualizar seus ganhos, enquanto o Budgets permite que você defina orçamentos e receba alertas quando seus custos se aproximam de um limite.

---

## Conceito chave: O Modelo de Responsabilidade Compartilhada
É fundamental entender que a nuvem não terceiriza a segurança. A responsabilidade é **compartilhada**.
* **A AWS é reponsável pela "segurança da nuvem":** Isso inclui proteger a infraestrutura global, o hardware, o software e as instalações físicas que rodam os serviços.
* **O cliente é responsável pela "segurança na nuvem":** Isso inclui proteger seu próprio código, seus dados, as configurações de rede (como Security Groups) e gerenciar as identidades de acesso (IAM).
  A vasta gama de serviços da AWS permite que você construa soluções de qualquer tamanho e complexidade, com a flexibilidade de escolher o nível de controle que melhor se adapta às suas necessidades de negócio.

<div align="right">
  <a href="#top">
    <img src="https://img.shields.io/badge/-Voltar%20ao%20Topo-lightgrey?style=for-the-badge" alt="Botão de voltar ao topo">
  </a>
</div>