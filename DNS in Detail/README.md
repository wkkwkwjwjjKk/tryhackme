🧪 WRITE-UP: DNS in Detail
🎯 Objetivo do módulo

Compreender como o Domain Name System funciona, sua hierarquia e como ele traduz nomes de domínio em endereços IP.

🌐 O que é DNS

DNS (Domain Name System) é um sistema responsável por traduzir nomes de domínio (ex: google.com) em endereços IP que computadores entendem.

🧠 Estrutura de um domínio

Um domínio é dividido em:

TLD (Top Level Domain): .com, .org, .br
SLD (Second Level Domain): nome principal (ex: tryhackme)
Subdomínio: parte à esquerda (ex: admin.tryhackme.com)
⚙️ Conceitos aprendidos
🔹 TLD

Tipo de domínio final, como:

gTLD: .com, .org, .net
ccTLD: .br, .uk, .jp
🔹 Subdomínios

Podem existir vários níveis:

admin.site.com
dev.api.site.com

Não existe limite de níveis, apenas limite de tamanho.

🔹 TTL (Time To Live)

Define por quanto tempo uma resposta DNS fica armazenada em cache.

🔹 DNS recursivo

Servidor (geralmente do ISP) que resolve nomes para o usuário automaticamente.

🧪 Ferramentas usadas
nslookup
conceitos de resolução DNS
🧠 Aprendizado prático

Durante o módulo, foi possível entender:

como domínios são estruturados em hierarquia
como a internet traduz nomes em IPs
como subdomínios podem revelar infraestrutura
como o DNS é essencial para reconhecimento em segurança
⚔️ Conexão com segurança ofensiva

O DNS é importante em pentest porque permite:

descoberta de subdomínios
mapeamento de infraestrutura
reconhecimento de superfícies de ataque
🚀 Conclusão

Este módulo serviu como base fundamental para entender como a internet funciona sob o ponto de vista de rede e segurança, preparando para técnicas de enumeração e reconhecimento em testes de intrusão.
