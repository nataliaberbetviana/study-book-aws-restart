<a id="top"></a>
# Modelos de Serviço e Implantação
## Modelos de Serviço: O que Você "aluga" da Nuvem
Para entender melhor, pense na metáfora de construir uma casa. Dependendo do serviço que você contrata, você tem mais ou menos controle sobre o processo.
### IaaS (Infrastructure as a Service)
* **O que é:** É o alicerce da nuvem. Com o IaaS, você aluga a **infraestrutura básica de TI**, como servidores virtuais, redes, armazenamento e sistemas operacionais. É a opção que te dá o **maior nível de controle**.
    * **Na prática:** O provedor de nuvem te dá a "casa" (servidores e rede), mas você é o responsável por tudo que está dentro dela: a mobília (SO), a decoração (aplicações) e a manutenção (gerenciamento).
    * **Melhor para:** Empresas que precisam de controle total do ambiente, desenvolvedores que querem criar ambientes personalizados, ou para migrar aplicações existentes de um data center local para a nuvem.
    * **Exemplos:** Usar a máquina virtual
### PaaS (Platform as a Service)
* **O que é:** O PaaS te dá um **ambiente de desenvolvimento e implantação completo**. Você não precisa se preocupar com o SO, hardware ou a infraestrutura subjacente. Apenas com seu código.
    *  **Na prática:** Voltando à nossa metáfora, no PaaS, você aluga um "apartamento mobiliado e com todos os utilitários". Você não precisa se preocupar com a rede elétrica ou a encanação, só em morar e usar o espaço. O provedor gerencia o SO, o middleware e as ferramentas de desenvolvimento.
    * **Melhor para:** Desenvolvedores e empresas que querem focar 100% na criação e no lançamento de suas aplicações, sem o trabalho de gerenciar a infraestrutura. Acelera o tempo de desenvolvimento e o lançamento de produtos.
    * **Exemplos:** **Heroku** para hospedar sites, **AWS Elastic Beanstalk** ou **Google App Engine**.
### SaaS (Software as a Service)
* **O que é:** O SaaS é o modelo mais comum e acessível. Você usa um **software pronto e completo** que é hospedado e gerenciado pelo provedor de nuvem. Tudo o que você precisa é de uma conexão com a internet.
    * **Na prática:** É como usar um "serviço de streaming" para assistir filmes. Você não se preocupa com o filme em si, com o servidor ou com a rede que o hospeda. Você simplesmente acessa a plataforma e usa o conteúdo. O provedor de nuvem gerencia tudo, desde a infraestrutura até o software e os dados.
    * **Melhor para:** Usuários finais e empresas que precisam de um software específico sem o trabalho de instalação, manutenção ou gerenciamento de infraestrutura.
    * **Exemplos:** **Gmail**, **Google Docs**, **Microsoft 365**, **Salesforce**, **Netflix** e **Dropbox**.

---

## Modelos de Implantação: Onde a Nuvem está Localizada
Esses modelos definem onde e como a estrutura de nuvem é mantida.
### Nuvem Pública
**O que é:** Os serviços de nuvem são fornecidos por terceiros e disponibilizados para o **pública em geral** pela internet. Os recursos são compartilhados entre os múltiplos clientes (multi-tenancy), mas são logicamente ligados.
* **Benefícios:** Escalabilidade quase ilimitada, pagamento por uso, alta disponibilidade e menor custo. Você se beneficia da economia de escala dos grandes provedores.
* **Desvantagens:** Menor controle sobre a infraestrutura e a segurança física.
* **Exemplos:** **AWS**, **Microsoft Azure** e **Google Cloud Platform (GCP)**.
### Nuvem Privada
**O que é:** Uma infraestrutura de nuvem **dedicada a um única organização**. Ela pode ser gerenciada internamente pela própria empresa ou por um terceiro.
* **Benefícios:** Maior controle, segurança e privacidade. Ideal para empresas com requisitos de segurança e conformidade.
* **Desvantagens:** Custo inicial e de manutenção mais alto, responsabilidade de gerenciamento da equipe interna. Menos escalável que a nuvem pública.
* **Exemplos:** Um banco que constrói e opera seu próprio data center de nuvem para garantir a conformidade regulatória.
### Nuvem Híbrida
**O que é:** Uma **combinação de nuvem pública e privada**. As duas infraestruturas são interligadas e permitem que dados e aplicações se movam entre elas.
* **Benefícios:** Combina o melhor de dois mundos. Você pode usar a nuvem privada para dados e aplicações sensíveis e a nuvem pública para lidar com cargas de trabalho variáveis ou não críticas. Oferece flexibilidade e otimização de custos.
* **Desvantagens:** Maior complexidade de gerenciamento.
* **Exemplos:** Uma empresa de varejo que usa a nuvem privada para seus dados de clientes (conformidade) e a nuvem pública para seu site de e-commerce, que precisa rodar rapidamente durante épocas de pico de vendas.


<div align="right">
  <a href="#top">
    <img src="https://img.shields.io/badge/-Voltar%20ao%20Topo-lightgrey?style=for-the-badge" alt="Botão de voltar ao topo">
  </a>
</div>

#