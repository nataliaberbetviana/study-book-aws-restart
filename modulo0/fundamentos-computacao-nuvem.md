# Fundamento da Computação em Nuvem
## O que é Computação em Nuvem?
* ***Definição e metáfora:** Entenda a computação em nuvem como o fornecimento de serviços de computação pela internet. Pense nela como a eletricidade: você não precisa construir uma usina para usar a luz, você apenas se conecta à rede elétrica. Com a nuvem, você não precisa comprar e manter servidores físicos, apenas se conecta ao provedor de nuvem.
* **Características Essenciais:**
	* **Elasticidade e Escalabilidade:** Capacidade de aumentar ou diminuir recursos de acordo com a demanda.
	* **Pagamento por uso (Pay-as-you-go):** Você só paga pelos recursos que consome.
	* **Acesso Amplo à Rede:** Acesso aos recursos a partir de qualquer lugar com internet.
	* **Serviço Sob Demanda:**  Você pode provisionar recursos por conta própria, sem a necessidade de interação.
---

## Modelos de Serviço e Implantação
* **Modelos de Serviço ( O que a Nuvem Oferece):**
	* **IaaS ( Infrastructure as a Service):** Você aluga a infraestrutura básica e gerencia o sistema operacional e as aplicações.
		* VM na AWS EC2.
	* **PaaS (Platform as a Service):** Você tem acesso a um ambiente completo para desenvolver, executar e gerenciar aplicações, sem se preocupar com a infraestrutura sibjacente.
		* Usar o Heroku para hospedar um site.
	* **SaaS (Software as a Service):** Você usa um software pronto para uso, acessível pela internet. O provedor de nuvem gerencia tudo.
		* Gmail, Microsoft 365, Salesforce.
* **Modelos de Implantação (Onde a Nuvem Está):**
	* **Nuvem Pública:** Serviços oferecidos por provedores como AWS, Google Cloud e Microsoft Azure para o público em geral.
	* **Nuvem Privada:** Infraestrutura de nuvem dedicada a uma única organização. Pode ser gerenciada pela própria empresa ou por um terceiro.
	* **Nuvem Híbrida:** Combinação de nuvem pública e privada. Permite que dados e aplicações se movam entre elas.
---

### Fundamentos de Rede na Nuvem (A Conexão Essencial)
* **Visão Geral:** A nuvem é, essencialmente, um enorme centro de dados que você acessa pela internet. A comunicação entre seu computador  e a nuvem depende de protocolos de rede.
* **O Protocolo IP (Internet Protocol):**
	* **O que é:** O IP é o sistema de endereçamento da internet. Pense nele como o endereço de uma casa. Cada dispositivo conectado à internet tem um endereço IP único que o identifica e permite que os dados cheguem ao destino correto.
	* **Função Principal:** Roteamento de pacotes. O IP é responsável por garantir que os pacotes de dados viajem do ponto A ao ponto B através de múltiplos roteadores e redes.
	* **Endereços IPv4 e IPv6:** Aprenda a diferença e por que o IPv6 é o futuro (e já o presente) da internet.
* **O Protocolo TCP (Transmission Control Protocol):**
	* **O que é:** O TCP é o "garçom" da internet. Ele garante que os dados cheguem ao destino de forma confiável, na ordem correta, e sem erros.
	* **Função Principal:** Confiabilidade. O TCP estabelece a conexão, divide os dados em pacotes, os envia e, se um pacote for perdido, ele pede para ser reenviado. Ele é o responsável por garantir que um arquivo que você baixa não chegue corrompido. Pense nele como a parte do serviço postal que envia uma notificação de recebimento.
	* **TCP vs. UDP:** Aprenda sobre UDP (User Datagram Protocol) e as diferenças. O UDP é mais rápido, mas não garante a entrega, sendo ideal para streaming de vídeos e jogos, onde a velocidade é mais importante que a perfeição.
* **O Protocolo DNS (Domain Name System):**
	* **O que é:** O DNS é o "livro de contatos" da internet. Ele traduz nomes de domínios legíveis por humanos para endereços IP numéricos que os computadores entendem.
	* **Função Principal:** Tradução de nomes para IPs. Quando você digita um site, seu computador pergunta a um servidor DNS qual é o endereço IP associado a esse nome, pra então poder se conectar a ele usando o IP. Sem o DNS, você precisaria decorar o endereço IP de cada site que quisesse visitar.
