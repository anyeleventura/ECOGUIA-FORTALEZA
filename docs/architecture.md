# Arquitetura do Sistema - EcoGuia Fortaleza

## Visão Geral

Esta documentação descreve a arquitetura da API EcoGuia Fortaleza, que integra sistemas heterogêneos para fornecer orientações sobre sustentabilidade urbana.

## Diagrama de Arquitetura

![Diagrama da Arquitetura do EcoGuia Fortaleza](./img/imagem.png)

## Componentes do Sistema

- **Cliente (Frontend):** Aplicativo mobile ou web que consome nossa API.

- **API EcoGuia Fortaleza (Backend):** Servidor principal desenvolvido em Node.js e Express. Responsável por receber as requisições, processar a lógica de negócio e se comunicar com os serviços externos.

- **Groq API:** Serviço de inteligência artificial que processa as perguntas dos usuários e gera respostas contextualizadas sobre sustentabilidade.

- **OpenWeatherMap API:** Serviço opcional que fornece dados climáticos para enriquecer as respostas com informações sobre o clima de Fortaleza.

## Fluxo de Dados

1. O usuário envia uma pergunta pelo aplicativo mobile para o endpoint `POST /api/ask` da nossa API.

2. A API valida a requisição e monta um prompt contextualizado.

3. A API envia o prompt para a Groq API usando o protocolo REST/HTTP.

4. A Groq API processa a solicitação e retorna uma resposta.

5. Nossa API recebe a resposta, formata adequadamente e a retorna para o aplicativo mobile.

6. O usuário recebe a resposta no aplicativo.

## Protocolos de Comunicação

- **REST/HTTP:** Protocolo principal utilizado para todas as comunicações entre o cliente, nossa API e as APIs externas.

- **JSON:** Formato de dados utilizado para o envio e recebimento de informações.