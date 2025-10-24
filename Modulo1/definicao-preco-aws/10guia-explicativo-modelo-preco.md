# 🎓 Guia Essencial para a Certificação AWS: Modelo de Preço e Fundamentos

### Módulo 1: A Filosofia Central do Preço AWS

A AWS adota uma abordagem de preços de **pagamento conforme o uso** (*Pay-as-you-go*), o que a torna semelhante a um serviço público, como energia ou água.

O objetivo central é a flexibilidade: você paga apenas pelos serviços individuais que precisa e pelo tempo que os utiliza, sem a necessidade de contratos de longo prazo ou taxas de cancelamento.

#### CapEx vs. OpEx: A Grande Mudança

Um conceito fundamental é a mudança de despesas:

*   **Infraestrutura Local (On-Premises):** Exige **Despesas de Capital (CapEx)**. São custos fixos e elevados iniciais (hardware, datacenters) que são difíceis de estimar e não diminuem se a capacidade for subutilizada.
*   **Nuvem AWS:** Permite a troca de CapEx por **Despesas Operacionais (OpEx)**. O pagamento é variável e baseado no consumo efetivo. Isso permite agilidade e escalabilidade, adaptando a empresa conforme a necessidade, e não com base em previsões.

### Módulo 2: Os Quatro Pilares do Modelo de Preço

Para otimizar os custos, a AWS utiliza quatro estratégias principais, que você deve conhecer a fundo:

#### 1. Pagamento Conforme o Uso (Pay-as-you-go)
Permite iniciar e interromper o uso de um produto a qualquer momento.
*   O custo de **Computação** (como EC2) é cobrado por hora ou por segundo.

#### 2. Pague Menos ao Fazer Reserva (Comprometimento)
Permite economizar significativamente em serviços como Amazon EC2 e Amazon RDS ao comprometer-se com um determinado nível de uso.

*   **Instâncias Reservadas (IR):**
    *   **AURI (Pagamento Total Antecipado):** Oferece o **maior desconto**.
    *   **PURI (Pagamento Antecipado Parcial):** Oferece descontos menores com menor gasto inicial.
    *   **NURI (Sem Pagamento Antecipado):** Oferece os menores descontos, sem gasto inicial.
*   **Savings Plans:** Modelo de precificação flexível que oferece economia substancial no uso de produtos de computação (Amazon EC2, AWS Lambda, AWS Fargate) e Machine Learning. Requer um compromisso de uso consistente (medido em USD/hora) por um ou três anos.

#### 3. Pague Menos ao Usar Mais (Descontos por Volume)
A utilização em maior volume resulta em custos mais baixos por unidade, aproveitando a economia de escala.
*   Para serviços como o **Amazon S3**, a definição de preço é feita em **camadas** (*tiered pricing*); quanto mais você usa por GB, menor será o preço por GB.

#### 4. Pague Menos à Medida que a AWS Cresce
A AWS foca na redução de custos operacionais e repassa essas economias aos clientes por meio de preços mais baixos ao longo do tempo.

### Módulo 3: Fatores Fundamentais de Custo (O que é Cobrado)

Três fatores determinam o custo da sua solução na AWS. Isso é um ponto de atenção crucial na prova:

1.  **Computação:** Cobrada por hora/segundo (dependendo do recurso), variando conforme o tipo de instância.
2.  **Armazenamento:** Cobrado normalmente por GB (ex: S3, EBS).
3.  **Transferência de Dados:**
    *   **Transferência de Saída (Egress):** Dados movidos para **fora da AWS** são agregados e cobrados por GB. Essa cobrança aparece no relatório mensal como *Transferência de dados para fora da AWS*.
    *   **Regra Essencial:** **Geralmente, não há cobrança** pela **transferência de dados de entrada** (para a AWS) ou pela transferência **entre serviços dentro da mesma Região da AWS**.

### Módulo 4: Ferramentas de Custo e Gerenciamento

#### 1. AWS Calculadora de Preços (AWS Pricing Calculator)
Esta é sua ferramenta obrigatória para estimar a fatura mensal.

*   **Propósito:** Gerar estimativas detalhadas de custos por serviço e por Região.
*   **Funcionalidade:** Permite modelar e comparar soluções complexas (como Recuperação de Desastre) e identificar oportunidades de redução de custos.
*   **Como Usar:** Para configurar uma estimativa, você deve selecionar uma **Região** e inserir as especificações (parâmetros) do serviço desejado (ex: Amazon EC2).

#### 2. Custo Total de Propriedade (TCO)
O TCO é a estimativa financeira utilizada para **comparar os custos diretos e indiretos** de uma infraestrutura local (*On-Premises*) versus a migração para a nuvem AWS.

### Módulo 5: Serviços Gratuitos

Você deve distinguir entre serviços gratuitos por um tempo limitado e serviços que não têm custo adicional:

*   **Nível Gratuito (Free Tier):** Aplicável a novos clientes por até um ano, permitindo a experiência prática em produtos específicos (ex: Microinstância T2 do EC2).
*   **Serviços Sem Custo Adicional:** Serviços que não incorrem em cobrança direta, embora possam provisionar recursos que serão cobrados em outros serviços. Exemplos importantes incluem:
    *   **Amazon VPC** (Virtual Private Cloud).
    *   **AWS IAM** (Identity and Access Management).
    *   **AWS Organizations** (para faturamento consolidado).
    *   **AWS CloudFormation**.

### Módulo 6: Contexto de Inovação (AWS re:Invent 2024 Recap)

Embora esses tópicos representem inovações recentes, eles destacam o foco contínuo da AWS em performance, custo-benefício e segurança, conceitos importantes para um profissional de nuvem:

#### 1. IA e Otimização de Custos

*   **Amazon Bedrock:** Serviço chave para IA generativa, oferecendo vários modelos e facilitando a criação de aplicações sem gerenciar infraestrutura complexa.
*   **Prompt Router:** Maximiza a performance e **minimiza os custos** ao encaminhar solicitações de IA para diferentes modelos de acordo com o melhor custo-benefício para a sua problemática.
*   **Model Distillation:** Recurso que permite criar um modelo de IA menor, mais rápido e **mais econômico** a partir de um modelo robusto do Bedrock, otimizando a quantidade de *prompts*.

#### 2. Segurança e Governança

*   **VPC Origin:** Uma atualização do CloudFront que aumenta a segurança ao permitir que a borda computacional aponte diretamente para a rede privada, reduzindo a exposição pública de serviços sensíveis (como EC2 e API Gateways).
*   **Amazon GuardDuty:** Serviço de proteção ativa que recebeu aprimoramento com o **Extended Threat Detection**, melhorando a precisão na identificação e rastreio de sequências de atividades de ameaças.
*   **Resource Control Policies:** Uma nova camada de controle de governança que oferece maior **granularidade** para os administradores de conta gerenciarem recursos em subcontas, mitigando o uso indevido.

#### 3. Banco de Dados

*   **Aurora Limitless:** Solução desenvolvida para aplicações de larga escala que garante integridade e confiabilidade em cargas massivas de trabalho. Ele segrega as funcionalidades de transações, dados e *storages* em APIs internas, combinando alta integridade com a disponibilidade que o *Serverless* (baseado em *Shards*) oferece.

---

# 🚀 Foco na Certificação: Pilares de Preço e Transferência de Dados

### Módulo 1: Os Quatro Pilares do Modelo de Preço da AWS

O modelo de preço da AWS é construído em uma filosofia de flexibilidade e consumo, permitindo que os clientes paguem apenas pelos serviços que consomem. Isso elimina a necessidade de grandes despesas iniciais (CapEx) e contratos de longo prazo.

Essas são as quatro estratégias mestras que a AWS utiliza para otimizar e reduzir seus custos:

#### 1. Pagamento Conforme o Uso (Pay-as-you-go)
Este pilar representa a mudança fundamental do modelo de TI tradicional para a nuvem.

*   **Substituição de Custos:** Você **troca Despesas de Capital (CapEx)**, que são custos fixos elevados (servidores, datacenters), por **Despesas Operacionais (OpEx)**, que são variáveis e baseadas no consumo real.
*   **Flexibilidade Total:** Você só paga pelos serviços individuais que precisar, pelo tempo que os utiliza, e pode iniciar e interromper o uso de um produto a qualquer momento.
*   **Cobrança:** O custo de serviços como computação é determinado pela capacidade por hora ou por segundo, dependendo do recurso.

#### 2. Pague Menos ao Fazer Reserva (Comprometimento)
Para cargas de trabalho previsíveis e constantes, a AWS recompensa o compromisso de longo prazo com descontos significativos.

*   **Instâncias Reservadas (IR):** Permitem economizar em serviços como Amazon EC2 e Amazon RDS. As opções de pagamento antecipado definem o nível de desconto:
    *   **AURI (Pagamento Total Antecipado):** Oferece o **maior desconto**.
    *   **PURI (Pagamento Antecipado Parcial):** Oferece descontos menores com menor gasto inicial.
    *   **NURI (Sem Pagamento Antecipado):** Oferece os menores descontos, sem nenhum gasto inicial.
*   **Savings Plans:** Este é um modelo de preço flexível que oferece economia em produtos de computação (como EC2, AWS Lambda, AWS Fargate) e Machine Learning. Requer um compromisso de uso consistente, medido em **USD/hora**, por um ou três anos.

#### 3. Pague Menos ao Usar Mais (Descontos por Volume / Economia de Escala)
À medida que seu uso aumenta, o custo por unidade diminui.

*   **Descontos Progressivos:** A utilização em maior volume resulta em custos mais baixos, permitindo que você se beneficie das economias de escala.
*   **Preços em Camadas (*Tiered Pricing*):** Para serviços como o **Amazon S3** e a transferência de dados **para fora** do EC2, a definição de preço é feita em camadas; quanto mais você usa por GB, menor é o preço por GB.

#### 4. Pague Menos à Medida que a AWS Cresce
A AWS foca constantemente na redução de seus custos operacionais e de hardware e repassa essas economias aos clientes através da redução de preços ao longo do tempo.

---

### Módulo 2: A Regra Essencial da Cobrança de Transferência de Dados

Para a certificação, você deve memorizar os **Três Fatores Fundamentais de Custo** e a regra crucial de transferência de dados:

Os custos da sua solução na AWS são determinados por:

1.  **Computação** (cobrada por hora/segundo).
2.  **Armazenamento** (cobrado por GB).
3.  **Transferência de Dados**.

#### A Transferência de Dados: O Ponto Chave

A regra de cobrança de transferência de dados é a mais frequentemente testada em exames de nível fundamental:

| Tipo de Transferência | Cobrança | Regra Essencial |
| :--- | :--- | :--- |
| **Entrada (Dados para a AWS)** | **Geralmente não há cobrança** | Os dados movidos *para* a AWS (Entrada) são, na maioria dos casos, gratuitos. |
| **Saída (Dados para Fora da AWS)** | **Cobrada por GB** | Os dados movidos *para fora* da AWS são agregados entre serviços e cobrados de acordo com a taxa de transferência de dados de saída. |
| **Transferência Interna** | **Geralmente não há cobrança** | A transferência de dados entre serviços **dentro da mesma Região da AWS** é, na maioria dos casos, gratuita. |

**Lembrete de Certificação:**

*   O custo de saída é exibido no relatório mensal como **Transferência de dados para fora da AWS**.
*   Quanto mais dados você transfere para fora, o preço por GB pode diminuir devido à definição de preços em camadas.

Dominando esses pilares e a regra da transferência de dados, você terá a base necessária para enfrentar as questões de custo e otimização da sua certificação!