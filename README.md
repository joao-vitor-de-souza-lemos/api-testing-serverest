# 🧪 API Testing — ServeRest

> Automação de testes de API REST utilizando Postman, com cobertura completa dos endpoints da plataforma [ServeRest](https://serverest.dev).

---

## 📌 Sobre o Projeto

Este repositório contém uma collection do Postman desenvolvida para testar a API pública **ServeRest**, uma API REST criada especificamente para fins educacionais na área de Quality Assurance.

Os testes cobrem os principais fluxos da aplicação — autenticação, cadastro de usuários, gerenciamento de produtos e operações de carrinho — com validações automatizadas de status code, tempo de resposta e integridade dos dados retornados.

---

## 🛠️ Tecnologias Utilizadas

- [Postman](https://www.postman.com/) — criação e execução das requisições e testes
- [ServeRest API](https://serverest.dev) — API REST pública para estudos de QA
- JavaScript — scripts de testes e pre-request scripts
- Git & GitHub — versionamento e hospedagem do projeto

---

## 📁 Estrutura do Repositório

```
api-testing-serverest/
├── collections/
│   └── Serverest_postman_collection.json   # Collection com todos os endpoints e testes
├── environments/
│   └── Serverest_Dev_postman_environment.json  # Variáveis de ambiente (Dev)
├── globals/
│   └── postman_globals.json                # Variáveis globais do Workspace
└── README.md
```

---

## 📋 Endpoints Cobertos

| Módulo     | Método | Endpoint                        | Descrição                        |
|------------|--------|---------------------------------|----------------------------------|
| Login      | POST   | `/login`                        | Autenticação e captura do token  |
| Usuário    | GET    | `/usuarios`                     | Listar todos os usuários         |
| Usuário    | GET    | `/usuarios/:id`                 | Buscar usuário por ID            |
| Usuário    | POST   | `/usuarios`                     | Cadastrar novo usuário           |
| Usuário    | PUT    | `/usuarios/:id`                 | Alterar dados de usuário         |
| Usuário    | DELETE | `/usuarios/:id`                 | Deletar usuário                  |
| Produto    | GET    | `/produtos`                     | Listar todos os produtos         |
| Produto    | GET    | `/produtos/:id`                 | Buscar produto por ID            |
| Produto    | POST   | `/produtos`                     | Criar novo produto               |
| Produto    | PUT    | `/produtos/:id`                 | Alterar produto                  |
| Produto    | DELETE | `/produtos/:id`                 | Deletar produto                  |
| Carrinho   | GET    | `/carrinhos`                    | Listar todos os carrinhos        |
| Carrinho   | GET    | `/carrinhos/:id`                | Buscar carrinho por ID           |
| Carrinho   | POST   | `/carrinhos`                    | Criar carrinho                   |
| Carrinho   | DELETE | `/carrinhos/concluir-compra`    | Concluir compra                  |
| Carrinho   | DELETE | `/carrinhos/cancelar-compra`    | Cancelar compra                  |

---

## ✅ Testes Automatizados Implementados

- Validação de **status code** nas respostas (201, 200)
- Verificação de **tempo de resposta** abaixo de 300ms
- Validação do **corpo da resposta** (mensagens e campos específicos)
- **Pre-request scripts** com geração de dados aleatórios (nome, e-mail)
- **Captura automática de token JWT** após login e repasse para requisições autenticadas
- Uso de **variáveis globais e de ambiente** para desacoplamento dos dados de teste

---

## 🚀 Como Importar e Executar

### Pré-requisitos

- [Postman](https://www.postman.com/downloads/) instalado

### Passo a passo

1. Clone ou faça o download deste repositório
2. Abra o Postman
3. Importe a collection: **Import → selecione** `collections/Serverest_postman_collection.json`
4. Importe o environment: **Import → selecione** `environments/Serverest_Dev_postman_environment.json`
5. Importe os globals: **Import → selecione** `globals/postman_globals.json`
6. Selecione o environment **Serverest Dev** no canto superior direito
7. Execute a collection pelo **Collection Runner** na ordem recomendada:
   - POST Cadastro de Usuário
   - POST Criar Produtos
   - GET Buscar produto único
   - DELETE Deletar produto

> ⚠️ Os arquivos de environment e globals não contêm valores sensíveis. Tokens e credenciais são gerados e gerenciados dinamicamente em tempo de execução pelos scripts da collection.

---

## 👤 Autor

**João Vitor de Souza Lemos**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-joaolemos2004-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/joaolemos2004)
[![GitHub](https://img.shields.io/badge/GitHub-joao--vitor--de--souza--lemos-black?style=flat&logo=github)](https://github.com/joao-vitor-de-souza-lemos)
