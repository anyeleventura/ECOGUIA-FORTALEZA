# Pedalaih: Plataforma Comunitária de Bicicletas Compartilhadas

![Status do Projeto](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)

Repositório central do projeto **Pedalaih**, uma plataforma de integração para um sistema de bicicletas compartilhadas com atualização comunitária.

### 1. Visão Geral e Objetivos

O objetivo deste trabalho é projetar e desenvolver uma API de integração para um sistema de bicicletas compartilhadas, focando em gerar impacto social positivo através da tecnologia. A solução funcional permite a comunicação entre diferentes sistemas (cliente e servidor) através de uma API RESTful, que servirá de base para um futuro sistema multiplataforma.

Os principais objetivos do sistema são:
* Aumentar a confiabilidade das informações de disponibilidade de bicicletas.
* Incentivar o uso de transporte sustentável.
* Fomentar o engajamento comunitário na manutenção de um bem coletivo.
* Aplicar conceitos de arquitetura de software e integração de sistemas em um projeto prático.

### 2. O Problema e a Justificativa

A mobilidade urbana em grandes cidades enfrenta o desafio da baixa adesão a transportes sustentáveis. Um dos principais obstáculos nos sistemas de bicicletas compartilhadas é a falta de informação confiável e em tempo real sobre a disponibilidade de bicicletas, o que gera frustração e desconfiança nos usuários. Este problema vai contra os princípios do **ODS 11: Cidades e Comunidades Sustentáveis**, que visa tornar os assentamentos humanos mais inclusivos, seguros, resilientes e sustentáveis. A solução proposta aborda diretamente este desafio.

### 3. A Solução Proposta e Escopo

A solução é a **Pedalaih**, uma plataforma onde a própria comunidade atualiza os dados de disponibilidade das bicicletas. Através de um aplicativo, o usuário poderá informar em tempo real quantas bicicletas estão em uma estação, criando um sistema de dados mais dinâmico e preciso.

**Escopo do Projeto (Etapa Atual):**
* **ETAPA 1:** Desenvolvimento e implementação de uma API RESTful funcional, com no mínimo dois endpoints, testes unitários e tratamento de erros.

### 4. Arquitetura da Solução

A arquitetura do sistema é baseada no modelo Cliente-Servidor. Uma API RESTful central (Backend) gerencia todas as regras de negócio e a comunicação com o banco de dados. Os Clientes (Frontend) consomem essa API para exibir e enviar informações.

**[INSERIR DIAGRAMA DA ARQUITETURA AQUI]**
*(Um diagrama visual mostrando o fluxo: Cliente Mobile/Web -> API Backend -> Banco de Dados)*

### 5. Tecnologias Propostas

| Categoria          | Tecnologia              |
| :----------------- | :---------------------- |
| **Backend (API)** | Node.js, Express.js     |
| **Frontend Web** | Html, JavaScript, Bootstrap      |
| **Banco de Dados** | MySql              |
| **Testes** | Jest, Supertest         |
| **Documentação** | Postman                 |

### 6. Documentação da API (Endpoints)

A seguir, as principais rotas da API desenvolvida.

| Verbo | Endpoint                  | Descrição                                        | Autenticação? |
| :---- | :------------------------ | :----------------------------------------------- | :------------ |
| `POST`| `/users`                  | Cadastra um novo usuário.                        | Não           |
| `POST`| `/login`                  | Autentica um usuário e retorna um token JWT.     | Não           |
| `GET` | `/stations`               | Lista todas as estações de bicicletas.           | Não           |
| `GET` | `/stations/:id`           | Retorna os detalhes de uma estação específica.   | Não           |
| `POST`| `/stations/:id/update`    | Atualiza a contagem de bicicletas de uma estação.| **Sim** |

### 7. Como Executar e Testar o Projeto

Siga as instruções abaixo para executar a API localmente e realizar testes.
**Pré-requisitos:**
* Node.js (v18+)
* Git
* Postman ou Insomnia

```bash
# 1. Clone o repositório
git clone [https://github.com/anyeleventura/pedalaih.git](https://github.com/anyeleventura/pedalaih.git)
cd pedalaih

# 2. Instale as dependências
npm install

# 3. Configure as variáveis de ambiente
# Renomeie o arquivo .env.example para .env e preencha com suas credenciais do banco de dados

# 4. Inicie a aplicação em modo de desenvolvimento
npm run dev

# 5. Rode os testes unitários
npm test
