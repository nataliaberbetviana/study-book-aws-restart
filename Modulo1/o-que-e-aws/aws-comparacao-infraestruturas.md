# Comparação de Infraestruturas
## Segurança
Em uma infraestrutura local, a segurança é uma responsabilidade exclusiva e complexa. Você deve gerenciar dispositivos físicos e a equipe de segurança. Na AWS, a segurança é um serviço compartilhado, com a AWS gerenciando a segurança **da** nuvem e você gerenciando a segurança **na** nuvem.
* **On Premise:** A segurança é implementada e mantida por meio de **Firewalls** físicos, **ACLs (Listas de Controle de Acesso)** e uma equipe de **Administradores de rede**.
* **AWS:** Substitui esses componentes por serviços virtuais. Os **Security Groups** atuam como firewalls virtuais para suas instâncias, as **ACLs de rede** controlam o tráfego de sub-redes, e o **IAM (Identify and Access Management)** gerencia o acesso de usuários e serviços, garantindo o privilégio mínimo.

---

## Networking (Rede)
Em um ambiente local, a rede exige hardware e cabeamento complexos. Na AWS, a rede é virtualizada e altamente configurável.
* **On Premise:** A infraestrutura de rede é composta por hardware físico, como **Roteadores**, **switches** e **Pipes de rede** para o transporte de dados.
* **AWS:** Oferece serviços para construir e gerenciar rua rede virtual. O **Amazon VPC (Virtual Private Cloud)** é a base, permitindo criar uma rede isolada na nuvem. O **Elastic Load Balancing** substitui a necessidade de balanceadores de cargas físicos, distribuindo o tráfego automaticamente para suas aplicações.

---

## Servidores
A Aquisição, configuração e manutenção de servidores físicos são tarefas custosas e demoradas. Na nuvem, os servidores são virtualizados, escaláveis e sob demanda.
* **On Premise:** Servidores físicos são comprados, instalados e mantidos por você, o que demanda um alto investimento inicial (CAPEX) e manutenção contínua.
* **AWS:** Servidores são instâncias virtuais. As **AMIs (Amazon Machine Images)** são modelos prontos pra lançar essas instâncias (servidores). As **instâncias** são os servidores virtuais que você pode ligar ou desligar em segundos, pagando apenas pelo tempo de uso.

---

## Armazenamento e Banco de Dados
O gerenciamento de armazenamento e bancos de dados em um ambiente local exige hardware dedicado e equipe especializada. A AWS simplifica isso com serviços gerenciados e escaláveis.
* **On Premise:** A solução de armazenamento depende de hardware físico, como **DAS (Direct Attached Storage)**, **SAN (Storage Area Network** e **NAS (Network Attached Strahe)**. Os bancos de dados (RDBMS) são executados em servidores próprios, com necessidade de gerenciamento manual.
* **AWS:** O armazenamento é oferecido em diferentes níveis de serviço:
    * **Amazon EBS ( Elastic Block Store):** Fornece volumes de armazenamento para suas instâncias.
    * **Amazon EFS (Elastic File System):** Oferece armazenamento de arquivos escalável.
    * **Amazon S3 (Simple Storage Service):** É ideal para objetos, como backups e arquivos estáticos.
    * **Amazon RDS (Relational Database Service):** Gerencia o banco de dados, cuidando de tarefas como backups, patches e escalabiliade.

---

## Conclusão
A principal diferença é a ** mudança de responsabilidade**. No modelo On Premise, você é responsável por todo o hardware e sua manunteç.ão. Na AWS, a responsabilidade de manter a infraestrutura subjacente é da Amazon, permitindo que você se concente na criação de aplicações e no crescimento do seu negócio. Essa transição reduz o custo inicial, aumenta a flexibilidade, e permite à escalabiliade de recurssos de forma rápida e eficiente.