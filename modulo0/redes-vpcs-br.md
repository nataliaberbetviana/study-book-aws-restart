<a id="top"></a>
# AWS e Cálculo de IP: entendendo a base da nuvem  
## 🌐 Computação em Nuvem: O Papel da Rede na AWS

Quando falamos em computação em nuvem, muita gente pensa logo em **escalabilidade**, **bancos de dados**, **inteligência artificial**, etc.  
Mas existe um detalhe que passa por baixo de alguns radares: **a rede**.

Na AWS (Amazon Web Services), tudo começa com a **VPC (Virtual Private Cloud)**, que nada mais é que uma rede virtual privada dentro da nuvem.  
Para criar essa VPC, precisamos escolher um **bloco de endereços IP**.

É aí que entra o famoso cálculo de IP.

---

## 🔎 O que é um bloco CIDR?

O bloco **CIDR (Classless Inter-Domain Routing)** define quantos endereços IP você terá à disposição.

**Exemplo:**
`10.0.0.0/16`


Esse `/16` significa que temos **65.536 endereços IP possíveis**.  
Parece muito, né? Mas, quando dividimos em sub-redes (**subnets**), esse número precisa ser bem planejado.

---

## 📚 Relembrando o básico de IP  

Um endereço IP é composto por:

- **Endereço de rede:** "nome" da rede.  
- **Endereço de hosts:** onde ficam os dispositivos/servidores.  
- **Broadcast:** responsável por envio de mensagens para todos os dispositivos conectados a uma mesma rede.

Por exemplo, no bloco:

> O bloco **CIDR /24** representa 256 endereços (de `192.168.1.0` até `192.168.1.255`).  
> - `.0` é a rede  
> - `.255` é a broadcast  
> - `.1` a `.254` ficam os hosts

Ou seja: `/24` significa que os primeiros **24 bits** são para a rede, sobrando **8 bits para os hosts**:  
`2^8 = 256 endereços`.

---

## 🚨 Por que planejar bem o CIDR é importante?

- Se escolhermos um bloco **muito pequeno**, pode faltar IP para futuros dispositivos.  
- Blocos **muito grandes** podem ser difíceis de dividir em subnets organizadas.

⚠️ **Atenção:** na AWS não é possível mudar o CIDR da VPC depois de criada (só adicionar blocos extras).

---

## 🌐 Subnets Públicas x Privadas

Dentro de uma VPC, criamos subnets para organizar a rede:

- **Subnet pública:** tem rota para a internet via *Internet Gateway*.  
- **Subnet privada:** não tem acesso direto à internet (ideal para bancos de dados e aplicações internas).

---

## ⚠️ Restrições da AWS

Um detalhe que muita gente esquece: **em cada subnet da AWS, 5 IPs são reservados automaticamente**.

**Exemplo: no bloco `10.0.0.0/24`**

- `.0` → endereço de rede  
- `.1` → reservado para o roteador da VPC  
- `.2` → reservado para DNS da AWS  
- `.3` → reservado para uso futuro  
- `.255` → broadcast  

Ou seja, um `/24` que deveria ter 256 IPs, **na prática terá 251 IPs utilizáveis** para o usuário final.

---

## 💡 Boas práticas

✅ Planeje sempre pensando no **crescimento futuro**.  
✅ Evite a **sobreposição de blocos CIDR**.  
✅ **Documente bem** a divisão de subnets e os usos de cada bloco.

---

## 📌 Conclusão

Entender e planejar **CIDR e subnets** na AWS é fundamental para criar redes **escaláveis**, **seguras** e **organizadas**.  
É a base que vai sustentar todas as aplicações que você colocar na nuvem.

---

## 📖 Aprofunde seu conhecimento

🔗 [Documentação oficial da AWS](https://docs.aws.amazon.com/)


<div align="right">
  <a href="#top">
    <img src="https://img.shields.io/badge/-Voltar%20ao%20Topo-lightgrey?style=for-the-badge" alt="Botão de voltar ao topo">
  </a>
</div>

#