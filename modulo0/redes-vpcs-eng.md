<a id="top"></a>
# AWS and IP Calculation: Understanding the Foundation of the Cloud  
## 🌐 Cloud Computing: The Role of Networking in AWS

When we talk about cloud computing, many people immediately think of **scalability**, **databases**, **artificial intelligence**, etc.  
But there is a detail that often flies under the radar: **the network**.

On AWS (Amazon Web Services), everything starts with the **VPC (Virtual Private Cloud)**, which is nothing more than a private virtual network inside the cloud.  
To create this VPC, we need to choose an **IP address block**.

This is where the famous IP calculation comes in.

---

## 🔎 What is a CIDR Block?

The **CIDR (Classless Inter-Domain Routing)** block defines how many IP addresses you will have available.

**Example:**  
`10.0.0.0/16`

This `/16` means we have **65,536 possible IP addresses**.  
Sounds like a lot, right? But when we divide them into **subnets**, this number needs to be carefully planned.

---

## 📚 Revisiting the Basics of IP  

An IP address is composed of:

- **Network address:** the "name" of the network.  
- **Host address:** where the devices/servers are located.  
- **Broadcast:** responsible for sending messages to all devices connected to the same network.

For example, in the block:

> The **CIDR /24** block represents 256 addresses (from `192.168.1.0` to `192.168.1.255`).  
> - `.0` is the network  
> - `.255` is the broadcast  
> - `.1` to `.254` are the hosts

In other words: `/24` means the first **24 bits** are reserved for the network, leaving **8 bits for the hosts**:  
`2^8 = 256 addresses`.

---

## 🚨 Why Proper CIDR Planning Matters

- If you choose a block that is **too small**, you might run out of IPs for future devices.  
- **Very large blocks** can be difficult to divide into organized subnets.

⚠️ **Attention:** On AWS, it is not possible to change a VPC’s CIDR block after creation (you can only add additional blocks).

---

## 🌐 Public vs. Private Subnets

Within a VPC, we create subnets to organize the network:

- **Public subnet:** has a route to the internet via an *Internet Gateway*.  
- **Private subnet:** does not have direct internet access (ideal for databases and internal applications).

---

## ⚠️ AWS Restrictions

One detail many people forget: **AWS automatically reserves 5 IP addresses per subnet**.

**Example: for the block `10.0.0.0/24`**

- `.0` → network address  
- `.1` → reserved for the VPC router  
- `.2` → reserved for AWS DNS  
- `.3` → reserved for future use  
- `.255` → broadcast  

So, a `/24` block that should have 256 IPs **actually has 251 usable IPs** for the end user.

---

## 💡 Best Practices

✅ Always plan with **future growth** in mind.  
✅ Avoid **overlapping CIDR blocks**.  
✅ **Document carefully** your subnet division and the purpose of each block.

---

## 📌 Conclusion

Understanding and planning **CIDR and subnets** on AWS is crucial for creating **scalable**, **secure**, and **well-organized** networks.  
This is the foundation that will support all the applications you deploy in the cloud.

---

## 📖 Learn More

🔗 [AWS Official Documentation](https://docs.aws.amazon.com/)

<div align="right">
  <a href="#top">
    <img src="https://img.shields.io/badge/-Voltar%20ao%20Topo-lightgrey?style=for-the-badge" alt="Botão de voltar ao topo">
  </a>
</div>

#