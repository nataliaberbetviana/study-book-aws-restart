<a id="top"></a>
# Modelo de Preço da AWS
Diferente de uma infraestrutura tradicional que exige um alto investimento inicial, o modelos de preço da AWS é baseado em **pagamento por uso**. A maioria dos custos é determinada por três fatores principais, que são a base para calcular o valor de quase todos os serviços.
## Computação
Esse é o custo do processamento em si, como o tempo em que um servidor virtual está ligado.
* **Cobrado por hora/segundo:** A maioria dos serviços de computação, como o Amazon EC2 e o AWS Lambda, cobra com base no tempo de uso. Para instâncias EC2 rodando no Linux, a cobrança é por segundo, com o mínimo de um minuto. Para Windows, a cobrança é por hora.
* **Varia por tipo de instância:** O preço da computação depende da **potência** do recurso. Um servidor com mais CPU, mais memória e mais capacidade de processamento custará mais por hora do que um servidor menor.

---

## Armazenamento
Este é p custo de guardar dados na nuvem.
* **Cobrado  por GB:** Serviços como o **Amazon S3** e o **Amazon EBS** precificam o armazenamento com base na quantidade de dados que você armazena em GB. Você paga pelo espaço que seus dados ocupam por mês.

---
## Transferência de Dados
Este é o custo da movimentação de dados dentro e fora da nuvem da AWS.
* **A entrada (inbound) não tem cobrança:** A transferência de dados da internet para a AWS geralmente **não é cobrada**. O custo é geralmente em GB. A cobrança é agregada, ou seja, o preço por GB pode diminuir à medida que o volume de dados transferidos aumenta.

---

## Conclusão
Compreender esses três fatores é crucial para otimizar os custos na AWS. O modelo de pagamento por uso permite que você escale seus recursos para cima ou para baixo de acordo com a demanda, garantindo que você pague apenas pelo que realmente usa.

<div align="right">
  <a href="#top">
    <img src="https://img.shields.io/badge/-Voltar%20ao%20Topo-lightgrey?style=for-the-badge" alt="Botão de voltar ao topo">
  </a>
</div>