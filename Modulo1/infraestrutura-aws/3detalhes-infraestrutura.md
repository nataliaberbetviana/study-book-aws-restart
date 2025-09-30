<a id="top"></a>
# A Infraestrutura Global da AWS em Detalhes
A AWS construiu uma das maiores e mais confiáveis redes de computação do mundo. Sua arquitetura é hierárquica e projetada para oferecer resiliência, baixa latência e conformidade regulatória.
## Data Centers da AWS
Os **Data Centers** são a base física da infraestrutura da AWS. Eles são enormes edifícios, com dezenas de milhares de servidores, onde os dados são armazenados e o processamento acontece.
* **Servidores Físicos:** Cada data center pode abrigar entre 50.000 e 80.000 servidores, todos interligados.
* **Sempre Ativos:** Para garantir a confiabilidade, todos os data centers da AWS estão sempre online. Nenhum servidor fica ocioso ou é desligado.
* **Hardware Personalizado:** A AWS utiliza hardware e protocolos de rede personalizados, projetados internamente para otimizar o desempenho e a segurança.

---

## Zonas de Disponibilidade (AZs)
As **Zonas de Disponibilidade (AZs)** são a próxima camada da arquitetura. Uma AZ é um ou mais data centers, próximos, mas isolados.
* **Isolamento de Falhas:** As AZs são projetadas para serem independentes em termos de energia, resfriamento e rede, garantindo que uma falha em uma AZ não afete outras.
* **Interconexão de Alta Velocidade:** Elas são conectadas por links de rede privados e de alta velocidade, o que permite que a comunicação entre elas seja rápida e segura.
* **Recomendação de Resiliência:** A AWS recomenda que os clientes repliquem seus dados e aplicações entre as AZs para fins de resiliência e alta disponibilidade. Se um data center falhar, a aplicação continua funcionando.

---

## Regiões da AWS
Uma **região** é uma área geográfica que contém duas ou mais AZs.
* **Isolamento Geográfico:** As regiões são geograficamente isoladas, o que é crucial para a recuperação de desastres.
* **Soberania de Dados:** O isolamento das regiões permite que as empresas atendam a requisitos de soberania de dados, mantendo os dados em um país específico.
* **Contole de Replicação:** O cliente tem total controle sobre a replicação de dados entre as regiões. Os dados não são replicados automaticamente, é uma escolha do usuário.

---

## Conclusão
A estrutura da AWS, com data centers agrupados em AZs e AZs agrupadas em Regiões, é a base da confiabilidade e flexibilidade que a nuvem oferece. Essa arquitetura permite que as empresas criem aplicações que não só são altamente disponíveis, mas também podem ser implantadas globalmente para atender a clientes em qualquer lugar do mundo.

<div align="right">
  <a href="#top">
    <img src="https://img.shields.io/badge/-Voltar%20ao%20Topo-lightgrey?style=for-the-badge" alt="Botão de voltar ao topo">
  </a>
</div>