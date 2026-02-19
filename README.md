# Implementação de Rede SOHO com Foco em Perícia Digital e Conectividade

## 📌 Visão Geral
Este projeto simula uma infraestrutura de rede Small Office/Home Office (SOHO) desenvolvida no Cisco Packet Tracer. O objetivo foi estabelecer conectividade entre uma LAN (Rede Local) e uma WAN (Internet Simulada), garantindo o tráfego de dados e a disponibilização de serviços de rede.

## 🛠️ Especificações Técnicas
* **Topologia:** Estrela.
* **Equipamentos:** Roteador ISR4331, Switch 2960, Servidor Genérico, PCs e Impressora.
* **Protocolos e Serviços:** DHCP (dinâmico), IPv4 Estático, HTTP e ICMP (Ping).

## 📊 Endereçamento Aplicado (Referência: Tabela do Curso)
| Dispositivo | IP | Máscara | Gateway |
| :--- | :--- | :--- | :--- |
| Admin PC | DHCP | - | 192.168.1.1 |
| Manager PC | DHCP | - | 192.168.1.1 |
| Printer | 192.168.1.100 | 255.255.255.0 | 192.168.1.1 |
| Web Server | 209.165.200.225 | 255.255.255.224 | 209.165.200.226 |

---

## ⚖️ Conexão com Cibersegurança e Perícia Forense
Este laboratório fornece a base técnica para investigações criminais modernas:

1. **Gestão de Logs e DHCP:** O entendimento de como o Roteador atribui IPs dinâmicos (DHCP) é fundamental para a correlação de eventos em perícias, permitindo identificar o suspeito através do histórico de concessão de endereços.
2. **Análise de Fluxo de Dados:** A configuração do Gateway Padrão e o tráfego HTTP permitem ao perito mapear rotas de exfiltração de dados e identificar possíveis pontos de interceptação (Sniffing).
3. **Persistência e Configuração:** A utilização do comando `write memory` no CLI demonstra a importância da integridade das configurações do ativo de rede durante uma análise post-mortem.

---

## 📸 Demonstração do Funcionamento
![Topologia da Rede](./evidencias/sua_imagem_da_topologia.png)
*Legenda: Conectividade estabelecida e luzes de interface em estado "Up".*

---

## 📜 Como replicar
1. Baixe o arquivo `.pkt` na pasta `/projeto-pkt/`.
2. Abra no Cisco Packet Tracer (v8.2 ou superior).
3. Realize um ping do `Admin PC` para o IP `209.165.200.225`.
