<a id="top"></a>
# Fundamentos de Rede na Nuvem - A Conexão Essencial
## O Protocolo IP (Internet Protocol)
O **IP** é a base da comunicação de dados na internet. Ele funciona como o sistema de endereçamento que garante que um pacote de dados enviado de seu computador chegue ao destino correto, seja um servidor de e-mail ou uma máquina virtual na nuvem.
* **Endereços IPv4 vs IPv6**
    * **IPv4:** É a versão mais antiga, usando 32 bits para criar endereços. O problema é que o número de endereços é limitado a cerca de 4,3 bilhões. Com a explosão de dispositivos conectados, esses endereços estão se esgotando rapidamente.
    * **IPv6:** A nova versão, que usa 128 bits, oferece um número praticamente ilimitado de endereços, resolvendo o problema de escassez e preparando a internet para o futuro. As redes de nuvem modernas já operam com IPv6.
* **Função de Roteamento:** Quando você envia um pacote de dados, ele não vai diretamente ao destino. Ele passa por vários **roteadores** no caminho. O protocolo IP é o responsável por incluir um cabeçalho do pacote para o endereço de destino. Cada roteador lê esse cabeçalho e encaminha o pacote para o próximo roteador no caminho até que ele chegue ao seu destino final.

---

## O Protocolo TCP (Transmission Control Protocol)
O **TCP** é construído sobre o IP e adiciona uma camada de **confiabilidade**. Ele não se preocupa com o endereço, mas sim com a garantia de que o pacote chegue ao destino **sem erros**, na ordem correta e de forma completa.
* **TCP vs. UDP (User Datagram Protocol)**
    * **TCP:** Pense no TCP como um serviço de entrega com recibo. Antes de enviar qualquer pacote de dados, ele estabelece uma conexão com o servidor ("three-way handshake"). Após o envio, ele espera por uma confirmação de recebimento. Se a confirmação não chegar, ele reenvia o pacote. Isso o torna ideal para transferências de arquivos, e-mails ou páginas web, onde a integridade é crucial.
    * **UDP:** Pense no UDP como um serviço de entrega sem rastreamento ou recibo. Ele simplesmente envia os pacotes de dados sem se preocupar em saber se eles chegaram ou não. Se um pacote for perdido, ele não será reenviado. Isso o torna mais rápido, sendo a escolha perfeita para aplicações que priorizam a velocidade em detrimento da confiabilidade total, como videochamadas, streaming de vídeo e jogos online. Um pequeno atraso ou perda de pacote em um jogo é preferível a ter a tela congelada enquanto o jogo espera por um pacote perdido.

---

## O Protocolo DNS (Domain Name System)
O **DNS** é essencial para a nossa experiência de navegação, pois ele lida com a parte da internet que é mais fácil para os humanos entenderem: os nomes.
* **Como o DNS funciona:** O processo de tradução é chamado de **resolução de nome**. Quando você digita "www.google.com" no seu navegador, o que acontecerá é o seguinte:
    * Seu computador envia uma solicitação a um **servidor DNS**.
    * O servidor DNS procura o endereço IP associado com o link.
    * Retorna o endereço IP do link para o seu computador.
      Esse processo acontece em milissegundos e é o que torna a internet acessível para nós. Sem o DNS, a navegação seria impossível, pois teríamos que memorizar uma longa lista de numeros para acessar nossos sites favoritos.

<div align="right">
  <a href="#top">
    <img src="https://img.shields.io/badge/-Voltar%20ao%20Topo-lightgrey?style=for-the-badge" alt="Botão de voltar ao topo">
  </a>
</div>

#