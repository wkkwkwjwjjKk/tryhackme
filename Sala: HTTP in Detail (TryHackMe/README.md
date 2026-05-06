📚 O que aprendi nessa sala

Nesta sala, consolidei os fundamentos do protocolo HTTP e sua importância no contexto de Web Hacking e segurança ofensiva.

Conceitos principais:

Diferença entre HTTP e HTTPS
Funcionamento de Requests e Responses
Métodos HTTP:
GET
POST
PUT
DELETE
Códigos de status:
2xx (sucesso)
3xx (redirecionamento)
4xx (erro do cliente)
5xx (erro do servidor)
Headers HTTP e sua importância
Funcionamento de Cookies e sua utilização em sessões

🧪 Parte prática (essencial)

Durante a prática, utilizei o navegador integrado da plataforma para manipular requisições HTTP e observar o comportamento do servidor.

Exemplos realizados:
GET /room
→ THM{YOU'RE_IN_THE_ROOM}
GET /blog?id=1
→ THM{YOU_FOUND_THE_BLOG}
DELETE /user/1
→ THM{USER_IS_DELETED}
PUT /user/2 com parâmetro:
username=admin
→ THM{USER_HAS_UPDATED}

POST /login

username = thm  
password = letmein  

→ Flag final: THM{HTTP_REQUEST_MASTER}

⚙️ Dificuldade e tempo

Dificuldade: Fácil
Tempo de conclusão: ~30–40 minutos

🧠 Conclusão

Essa sala é fundamental para entender como a web realmente funciona por baixo dos panos.

HTTP não é só teoria — ele é a base de tudo em:

Web Hacking
Bug Bounty
Red Team

Entender métodos, headers e cookies é essencial para qualquer pessoa que queira evoluir em segurança ofensiva.
