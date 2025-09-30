<a id="top"></a>
# A Infraestrutura Global da AWS
A infraestrutura global da AWS é a base física que sustenta todos os serviços da nuvem. Ela foi projetada para oferecer um ambiente de computação flexível, confiável, escalável e seguro, com uma rede global de alta qualidade.
## Componentes da Infraestrutura Global
A AWS divide sua infraestrutura em dois componentes principais para garantir a alta disponibilidade e a baixa latência para os clientes ao redor do mundo:
* **Regiões (regions):** As regiões são grandes localizações geográficas que abrigam múltiplos data centers. Cada região é fisicamente isolada das outras pra garantir que um desastre natural ou falha em uma delas não afete as demais.
* **Zonas de Disponibilidade (Availability Zones - AZs):** Dentro de cada região, existem as Zonas de Disponibilidade. Uma AZ é um ou mais data centers discretos, com energia, resfriamento e rede redundantes. Elas são fisicamente separadas, mas próximas o suficiente para ter conexões de rede de baixa latência. A criação de recursos em múltiplas AZs dentro de uma região é a forma como a AWS garante a alta disponibilidade.

---

## Como a Rede Global Funciona
Todos esses componentes são interligados por uma **rede de backbone de fibra óptica global** de alta velocidade. Essa rede permite que os dados viajem rapidamente entre as regiões, o que é crucial para aplicações que operam em escala global.
### Por que essa infraestrutura é importante?
* **Flexibilidade:** A existência de regiões e AZs em diferentes partes do mundo permite que as empresas escolham onde hospedar seus dados e aplicações, atendendo a requisitos de latência, soberania de dados e conformidade regulatória.
* **Confiança:** Ao distribuir recursos em múltiplas AZs, as aplicações se tornam resilientes a falhas de hardware e até mesmo a desastres naturais, pois uma falha em um AZ não afeta as outras.
* **Escalabilidade:** A capacidade de adicionar recursos sob demanda em qualquer região permite que as empresas expandam suas operações globalmente de forma rápida e eficiente.
* **Desempenho:** A rede de alta qualidade garante que os usuários finais tenham uma experiência rápida e fluida, independentemente de sua localização.

<div align="right">
  <a href="#top">
    <img src="https://img.shields.io/badge/-Voltar%20ao%20Topo-lightgrey?style=for-the-badge" alt="Botão de voltar ao topo">
  </a>
</div>