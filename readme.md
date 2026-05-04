# OWASP Juice Shop - Cybersec Project

Este projeto foi criado com o objetivo de **aprender cybersegurança na prática** utilizando o **OWASP Juice Shop**, uma aplicação web intencionalmente vulnerável e amplamente usada para treinamento em segurança ofensiva e defensiva.

## Objetivo

Desenvolver conhecimentos em:

- Fundamentos de segurança de aplicações web
- Identificação e exploração de vulnerabilidades comuns
- Boas práticas de mitigação e hardening
- Metodologia de testes de segurança (pentest em ambiente controlado)

## Sobre o OWASP Juice Shop

O OWASP Juice Shop é um laboratório interativo que contém desafios reais baseados em falhas conhecidas, como:

- SQL Injection
- XSS (Cross-Site Scripting)
- Broken Authentication
- Controle de acesso inadequado
- Exposição de dados sensíveis

Esses desafios ajudam a entender como ataques funcionam e como preveni-los.

## Como iniciar o projeto?
#### Pré-requisitos

- Node.js (versão 18 ou superior)
- npm (geralmente já vem com o Node)
- Docker (opcional)

---

### Método 1 — Usando Docker (mais simples)

```bash
docker run --rm -p 3000:3000 bkimminich/juice-shop
```

### Método 2 — Localmente com Nodejs

```
git clone https://github.com/juice-shop/juice-shop.git
cd juice-shop

#Instale as dependências:

npm install

#Inicie a aplicação:

npm start

#Acesse:

http://localhost:3000

```



## Estrutura de estudo sugerida

1. Configurar e executar o ambiente local
2. Explorar a aplicação e mapear funcionalidades
3. Resolver desafios por níveis de dificuldade
4. Documentar cada vulnerabilidade encontrada:
   - Descrição
   - Impacto
   - Passos para reprodução
   - Recomendação de correção
5. Revisar conceitos com base no OWASP Top 10

## Boas práticas durante o projeto

- Realizar testes **somente em ambiente local/laboratório**
- Não aplicar técnicas em sistemas sem autorização
- Registrar aprendizados e evidências técnicas
- Priorizar entendimento do risco e da mitigação

## Estrutura do Projeto

OWASP-JuiceShop-CybersecProject/
├── README.md                  ← visão geral do projeto
├── writeups/
│   ├── 01-reconhecimento.md
│   ├── 02-autenticacao-idor.md
│   ├── 03-sql-injection.md
│   ├── 04-xss.md
│   └── 05-avancado.md
├── scripts/
│   └── sqli-extractor.py      ← se você escrever algo
├── payloads/
│   └── xss-payloads.txt
└── relatorio-final.md

## Aviso legal

Este projeto é estritamente educacional. Todo uso deve respeitar princípios éticos e legislação vigente.
