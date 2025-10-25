# 1. Famílias e Tipos de Instância EC2

As instâncias EC2 são oferecidas em diversas famílias, cada uma otimizada para um caso de uso específico, variando as combinações de CPU, memória, armazenamento e capacidade de rede.

| Categoria | Famílias Típicas | Casos de Uso Principais |
| :--- | :--- | :--- |
| **Uso Geral** | **M** (M7, M6, M5), **T** (T2, T3, T4g) | Oferecem um **equilíbrio** de recursos (CPU, memória). Ideais para web servers, pequenos/médios bancos de dados ou ambientes de desenvolvimento/teste. |
| **Otimizadas para Computação** | **C** (C7, C6, C5) | Indicadas para cargas de trabalho que exigem **alto desempenho de CPU**. Usadas para processamento em *batch*, modelagem científica e *web servers* de alto desempenho. |
| **Otimizadas para Memória** | **R** (R8, R7, R6, R5), **X**, **High Memory** | Perfeitas para aplicações que processam **grandes conjuntos de dados na memória**. Incluem bancos de dados de alto desempenho (SAP HANA, Oracle DB, Microsoft SQL Server) e Big Data Analytics. |
| **Otimizadas para Armazenamento** | **I** (I4, I3), **D** (D2, D3), **H1** | Projetadas para cargas de trabalho que requerem **alto I/O sequencial** para grandes conjuntos de dados em armazenamento local. Exemplos: sistemas de arquivos distribuídos, *data warehousing* e bancos de dados NoSQL (MongoDB, Cassandra). |
| **Computação Acelerada** | **P, G, F, Inf** (P5, G6, Inf2) | Para aplicações que se beneficiam de **aceleração de hardware** (GPUs, FPGAs). Usadas em Machine Learning (ML), HPC e renderização gráfica. |

## Conceitos Chave de Tipos de Instância:

*   **Instâncias *Burstable***: As famílias **T2** e **T3** são *burstable*, o que significa que têm um desempenho bom para cargas de trabalho que não usam a CPU frequentemente, mas ocasionalmente precisam de um *burst* para um desempenho superior. O tipo T3 é a próxima geração do T2, oferecendo mais poder de computação a um custo mais baixo.
*   **Instâncias Graviton:** Instâncias como **M6g** e **T4g** usam processadores Graviton projetados pela AWS (baseados em ARM), que podem oferecer **até 40% de melhor preço/desempenho** em comparação com instâncias x86 comparáveis.
*   **Convenção de Nomenclatura:** Um nome como `t3.large` indica: `t` (Família), `3` (Geração do hardware) e `large` (Tamanho, definindo vCPU, Memória, etc.).
*   **Bare Metal vs. Virtualizada:** Instâncias **Bare Metal** (como as `*.metal`) fornecem acesso direto ao hardware físico subjacente, eliminando a camada do *hypervisor*, o que é crucial para baixa latência e requisitos de segurança estritos. Instâncias **Virtualizadas** (como `nano`, `2xlarge`, etc.) são fatias da capacidade de um servidor físico e são isoladas usando o *hypervisor* da AWS.

# 2. Modelos de Preço EC2

A escolha do modelo de preço tem um impacto significativo na eficiência de custos.

| Modelo de Preço | Desconto em Relação ao Sob Demanda | Flexibilidade | Caso de Uso Ideal |
| :--- | :--- | :--- | :--- |
| **Sob Demanda (On-Demand)** | 0% (Preço total) | **Máxima** | Cargas de trabalho curtas, imprevisíveis, ou em picos (desenvolvimento/teste). |
| **Instâncias Reservadas (RIs)** | Até **75%** (Standard RI) | **Mínima** (Compromisso com tipo, tamanho e região específicos) | Cargas de trabalho estáveis e previsíveis de 1 ou 3 anos. **Apenas Standard RIs podem reservar capacidade**. |
| **Savings Plans (SPs)** | Até **72%** (EC2 SP) ou **66%** (Compute SP) | **Alta** (Compromisso em gasto/hora) | Cargas de trabalho dinâmicas. SPs não reservam capacidade, mas aplicam descontos automaticamente ao uso elegível. |
| **Instâncias Spot** | Até **90%** | Sujeito a Interrupção | Cargas de trabalho tolerantes a falhas ou de grande escala (web back-ends, Big Data). A AWS pode retomar a capacidade a qualquer momento (com aviso de 2 minutos). |
| **Hosts Dedicados** | Varia | Controle de Hardware | Restrições de licenciamento de software (por soquete, núcleo) ou requisitos de conformidade. |

## Savings Plans vs. Reserved Instances (RIs)

Para a certificação, é vital entender a diferença de flexibilidade:

*   **RIs Padrão:** Oferecem os descontos mais altos (até 75%). São rígidas, exigindo compromisso com tipo, tamanho, plataforma e região exatos.
*   **Savings Plans de Computação (Compute SPs):** Oferecem a maior flexibilidade, pois o desconto se aplica a EC2, Fargate e Lambda, independentemente da família, tamanho ou região. O desconto é ligeiramente menor (até 66%).
*   **RIs Padrão** com escopo zonal são o *único* modelo que garante a **reserva de capacidade** dentro de uma *Availability Zone* (AZ) específica.

# 3. O Processo de Execução e o Ciclo de Vida

Ao lançar uma instância (o termo usado para criar uma instância EC2), nove decisões essenciais são tomadas no assistente:

1.  **AMI (Amazon Machine Image):** O modelo que contém o sistema operacional, software e configurações iniciais.
2.  **Tipo de Instância:** Seleciona o hardware (vCPU, Memória, etc.).
3.  **Definições de Rede:** Especifica a **VPC** e a **sub-rede**.
4.  **Função do IAM:** (Opcional) Concede permissões à instância para interagir com outros serviços AWS (ex.: Amazon S3).
5.  **Dados do Usuário (User Data):** Um script executado na **primeira inicialização** para automatizar a configuração.
    *   No Linux, pode ser *shell scripts* ou diretivas *cloud-init*.
    *   No Windows, usa-se tags `<script>` ou `<powershell>`.
    *   O *user data* é limitado a 16 KB.
6.  **Opções de Armazenamento:** Configura o **Volume Raiz** (normalmente Amazon EBS).
7.  **Tags:** Rótulos chave/valor para organização e alocação de custos.
8.  **Security Group:** Atua como um **firewall virtual** que controla o tráfego de entrada e saída.
9.  **Par de Chaves (Key Pair):** Usado para autenticação segura (via **SSH** para Linux ou para obter a senha no Windows).

## Ciclo de Vida da Instância

Os estados principais de uma instância são:

*   **Pendente (Pending):** Estado inicial durante o provisionamento.
*   **Em execução (Running):** Instância totalmente operacional.
*   **Interrompida (Stopped):** (Apenas para instâncias com volumes raiz EBS) A instância não incorre em custos de computação e pode ser reiniciada posteriormente. O volume raiz EBS persiste.
*   **Encerrada (Terminated):** A instância é excluída permanentemente e **não pode ser reiniciada**. Todos os volumes EBS configurados para exclusão na terminação são permanentemente deletados.

# 4. Amazon EC2 Auto Scaling

O Amazon EC2 Auto Scaling é essencial para arquiteturas resilientes e econômicas.

*   **Melhor Tolerância a Falhas:** Pode detectar quando uma instância está não saudável (unhealthy), encerrá-la e lançar uma substituta. Pode também ser configurado para usar múltiplas **Availability Zones** (AZs), lançando instâncias em outra AZ se uma ficar indisponível.
*   **Melhor Disponibilidade:** Garante que a aplicação tenha a quantidade certa de capacidade para lidar com a demanda de tráfego.
*   **Melhor Gerenciamento de Custos:** Aumenta e diminui a capacidade dinamicamente, permitindo que você pague apenas pelas instâncias usadas, encerrando-as quando não são mais necessárias.
*   **Distribuição de Instâncias:** O Auto Scaling tenta manter números equivalentes de instâncias em cada AZ habilitada para alta disponibilidade e confiabilidade.

# 5. Segurança e Conectividade

*   **Security Groups:** Agem como um firewall virtual para controlar o tráfego de entrada (inbound) e saída (outbound) da instância. É crucial garantir que o Security Group permita o tráfego SSH (porta 22) de seu IP para se conectar a uma instância Linux.
*   **Par de Chaves:** É usado para autenticar conexões seguras. Para instâncias Linux, você usa o cliente SSH e a chave privada (.pem).
*   **Nomes de Usuário Padrão (para SSH):** Para se conectar a uma instância, você precisa do nome de usuário correto dependendo da AMI:
    *   **Amazon Linux:** `ec2-user`
    *   **Ubuntu:** `ubuntu`
    *   **CentOS:** `centos` ou `ec2-user`
    *   **RHEL:** `ec2-user` ou `root`.

*   **Conectividade de Rede:** Erros de "Connection timed out" (conexão expirada) são frequentemente causados por Security Groups ou Network ACLs (ACLs de Rede) que bloqueiam o tráfego SSH (Porta 22).

