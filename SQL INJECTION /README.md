

**SQL Injection Examples - TryHackMe Writeup**

**Room:** SQL Injection Examples  
**Plataforma:** TryHackMe  
**Dificuldade:** Médio  

---

## **🎯 Níveis Completados**

### **Level 1 - Union-Based SQL Injection**
- **Técnica:** In-Band (Union + Error Based)
- **Payload principal:**
  ```sql
  0 UNION SELECT 1,2,group_concat(username,':',password SEPARATOR '<br>') FROM staff_users
  ```
- Extração das credenciais da tabela `staff_users`.

---

### **Level 2 - Blind SQLi (Authentication Bypass)**
- **Técnica:** Bypass de login
- **Payload:**
  ```sql
  ' OR 1=1;--
  ```
- **Flag:** `THM{SQL_INJECTION_3840}`

---

### **Level 3 - Boolean Based Blind SQLi**
- **Técnica:** Extração caractere por caractere (`LIKE 'X%'`)
- Senha descoberta: `3845`
- **Flag:** `THM{SQL_INJECTION_9581}`

---

### **Level 4 - Time Based Blind SQLi**
- **Técnica:** Exploração baseada em tempo usando `SLEEP()`
- **Payload principal:**
  ```sql
  admin123' UNION SELECT SLEEP(5);--
  ```
- **Flag:** `SQL_INJECTION_MASTER`

---

## **🧠 Conceitos Aprendidos**

- SQL Injection In-Band (Union e Error-Based)
- Blind SQL Injection (Boolean-Based e Time-Based)
- Bypass de autenticação
- Enumeração de banco de dados sem feedback visual
- Uso de `UNION SELECT`, `information_schema`, `SLEEP()`
- Importância de Prepared Statements como proteção

---

## **🛡️ Medidas de Proteção Recomendadas**

- Prepared Statements / Parameterized Queries
- Validação e sanitização de entradas
- Uso de ORM com cuidado
- Princípio do menor privilégio no banco de dados

---

**Tags:** `#SQLInjection #BlindSQLi #TryHackMe #WebSecurity #CyberSecurity`

---

