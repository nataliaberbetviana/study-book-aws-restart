<a id="top"></a>
# A Estrutura da Infraestrutura Global e dos Serviços da AWS
A AWS construiu sua nuvem sobre uma vasta infraestrutura física, que se traduz em um ecossistema de serviços projetados para serem escaláveis, confiáveis e de alta performance.
## A Infraestrutura Física
A fundação da AWS é sua rede global:
* **Regiões:** São grandes áreas geográficas, como **São Paulo** ou **Oregon**, onde a AWS agrupa seus data centers. Elas são fisicamente isoladas umas das outras para garantir que uma falha ou desastre em uma região não afete as outras.
* **Zona de Disponibilidade (AZs):** Dentro de cada região, existem múltiplas AZs. Umma AZ consiste em um ou mais data centers com energia, rede e resfriamento independentes. A prática recomendada é usar várias AZs para garantir a alta disponibilidade da API.
* **Pontos de Presença (PoPs):** São localizações globais usadas para serviços de borda da rede, como o **Amazon CloudFront**, que entrega conteúdo de baixa latência para os usuários finais, fazendo a comunicação entre regiões e o resto do mundo.

---

## A Hierarquia de Serviços
Sobre essa infraestrutura física, a AWS constrói seu vasto catálogo de serviços, que podem ser vistos em camadas de abstração.
* **Serviços Básicos:** Esta é a camada fundamental, composta pelos blocos de construção da nuvem.
    * **Computação:** Onde seu código é executado. Inclui o **Amazon EC2**, **Auto Scaling** e **Balanceamento de Carga**.
    * **Redes:**  Cuida da conectividade e segurança. A **Amazon VPC** permite que você crie redes virtuais isoladas na nuvem.
    * **Armazenamento:** Serviços para guardar dados, como o **Amazon S3** e **Amazon EBS**.
* **Serviços de Plataforma:** Esta camada oferece ferramentas mais especializadas que simplificam o desenvolvimento.
    * **Bancos de Dados:** Inclui opções como bancos de dados **Relacionais** e **NoSQL**.
    * **Serviços de Aplicações:** Ferramentas para a comunicação e processamento de dados, como **Filas de Mensagensa** e **Streaming de Dados)**.
    * **Ferramentas de DevOps:** A camada mais alta, com soluções completas para uso direto. Inclui **Desktops Virtuais** e ferramentas de **Colaboração** e **Análise**.

---

## Conclusão
A AWS não é apenas um conjunto de servidores, mas um ecossistema integrado. A infraestrutura física fornece a base de confiabilidade e desempenho, enquanto a hierarquia de serviços permite que os usuários escolham o nível de abstração que mais se adequa às suas necessidades, desde o controle total de um servidor até soluções completas e gerenciadas.

<div align="right">
  <a href="#top">
    <img src="https://img.shields.io/badge/-Voltar%20ao%20Topo-lightgrey?style=for-the-badge" alt="Botão de voltar ao topo">
  </a>
</div>