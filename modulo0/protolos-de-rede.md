<a id="top"></a>
# Uma Jornada pelas Camadas de Protocolos da Internet
## 🌐 Introdução: A Linguagem da Internet e o Modelo de Camadas 
Imagine a internet como uma grande e complexa rede de comunicação. Para que dispositivos de diferentes fabricantes consigam falar entre si, eles seguem um conjunto de regras, ou protocolos. Esses protocolos são organizados em camadas, onde cada camada tem uma função específica e se comunica com as camadas acima e abaixo dela.

As duas estruturas de camada mais importantes para entender as redes são: Modelo OSI (7 camadas) e o Modelo TCP/IP (4 camadas).

## 💻 Uma Visão Prática 
<img width="641" height="455" alt="image" src="https://github.com/user-attachments/assets/934faf82-64c1-426b-b880-74f08d2c4883" />
<br>
Este diagrama compara a estrutura de 7 camadas do Modelo OSI, com a estrutura de 4 camadas do Modelo TCP/IP. As caixas no centro mostram os protocolos mais comuns e em quais camadas eles operam em ambos os modelos.

## 📱 Camada de Aplicação do TCP/IP
Agrupa os protocolos que operam nas camadas de aplicação, apresentação (traduz e formata dados - critptografia e compressão) e sessão (gerencia a "conversa" entre dispositivos) do Modelo OSI.

É a camada mais próxima do usuário e onde os aplicativos e serviços interagem com os dados

* HTTP (protocolo da web) 
* DNS (traduz nome de domínio pra endereço IP) 
* DHCP (atribui endereços IP automaticamente aos dispositivos) 
* FTP (transferir arquivos)

## 📦 Camada de Transporte do TCP/IP
Presente de forma equivalente nos dois modelos, é responsável por gerenciar a comunicação entre dois dispositivos, garantindo a entrega dos dados. 

* TCP (garante a entrega confiável e ordenada dos dados - web e e-mail) 
* UDP (entrega rápida, mas sem garantia - streaming de vídeo e jogos online)

## ➡️ Camada de Internet do TCP/IP
Essa camada lida com o roteamento dos dados entre redes, sendo o IP o principal, pois é o responsável por endereçar e encaminhar pacotes de dados. No Modelo OSI é conhecida por camada de rede.

* IP (roteamento lógico dos pacotes) 
* ICMP (diagnóstico de rede e reporte de erro)

## 🔌 Camada de Acesso à Rede do TCP/IP
É a camada mais baixa, lidando com conexões físicas (como cabos e Wi-Fi) e equivale às camadas de enlace de dados (controla o fluxo de dados em um link físico) e física (lida com o meio de transmissão físico) do Modelo OSI.

* Ethernet (redes com fio) 
* Wi-fi 
* ARP (traduz IP em endereços físics - MAC)

## 📈 Como funciona o fluxo de dados
Quando você envia uma mensagem, os dados passam pela camada de aplicação, são processados pelo TCP ou UDP na camada de transporte, recebem um endereço IP na camada de internet, e são enviados como bits pela camada de acesso à rede. No destino o processo é invertido: os dados sobem pelas camadas até a aplicação, onde a mensagem é lida.

## 💡 Conclusão
A complexa teia da internet é construída sobre uma base sólida de protocolos organizados em camadas. O Modelo TCP/IP se destaca como a arquitetura prática que viabiliza a comunicação diária na web, enquanto o Modelo OSI serve como um mapa conceitual detalhado.
Juntos, esses modelos explicam como dados, transformados em bits, viajam do seu computador para qualquer lugar do mundo, provando que a "magia" da internet é, na verdade, um sistema incrivelmente lógico e bem organizado.

📚 Aprofunde seu Conhecimento
Para explorar as especificações técnicas, acesse a documentação oficial do [Protocolo TCP](https://datatracker.ietf.org/doc/html/rfc793) e o [Protocolo IP](https://datatracker.ietf.org/doc/html/rfc791).


<div align="right">
  <a href="#top">
    <img src="https://img.shields.io/badge/-Voltar%20ao%20Topo-lightgrey?style=for-the-badge" alt="Botão de voltar ao topo">
  </a>
</div>

#
