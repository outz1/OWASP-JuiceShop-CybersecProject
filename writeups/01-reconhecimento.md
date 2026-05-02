# Introdução


## Estrutura da Página

1. Página inicial         
2. /#/register            
3. /#/login               
4. /#/search?q=apple   
5. Clicar em um produto   
6. /#/basket             
7. /#/contact            
8. /#/about               
9. /#/profile             


- Inúmeros campos de input
- Rotas em main.js
- Funcionalidade de Chatbot
- 403 ao tentar entrar em /administration



## Rotas identificcadas com Burp

GET /rest/products/search?q= — campo de busca, altamente suspeito para SQLi
GET /api/Challenges/?name=Score%20B... — lista de desafios da aplicação
GET /api/Quantitys/ — endpoint de quantidades
GET /rest/admin/application-version — expõe versão da aplicação (retornou 200!)
GET /rest/admin/application-configuration — configuração do admin exposta!
GET /rest/languages — idiomas disponíveis
POST /socket.io/... — comunicação em tempo real via WebSocket


## ENDPOINTS ADMINISTRATIVOS SEM AUTENTICAÇÃO


- GET /rest/admin/application-version HTTP/1.1 → versão 19.2.1 exposta


- GET /rest/admin/application-configuration HTTP/1.1 → configuração completa exposta
```
 Scoreboard de gamificação do site e introdução aos desafios do projeto OWASP Juiche SHop
```

## IMPACTO
- Versão da aplicação permite busca de CVEs
- Usuários do sistema enumerados via reviews
- Rotas ocultas descobertas: /#/score-board, /#/bee-haven
- Respostas de perguntas de segurança expostas em plaintext

## Severity
Alta — informação sensível acessível sem qualquer autenticação