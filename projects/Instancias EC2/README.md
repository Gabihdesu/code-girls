# Chatbot com IA Generativa na AWS
## 📋 Descrição do Projeto

Este projeto consiste em um chatbot inteligente hospedado na AWS, utilizando ferramentas como o Amazon Lex, AWS Lambda e Amazon Bedrock (ou OpenAI via API externa) para criar um sistema de interação com o usuário em linguagem natural. O bot pode realizar tarefas de atendimento ao cliente, suporte técnico automatizado, assistente corporativo e muito mais.

### O foco é fornecer um chatbot que:

- Entende a linguagem natural com base em intenções e slots.

- Responde com lógica contextual, utilizando IA generativa para fornecer respostas mais sofisticadas.

- Armazena o histórico de interações para melhorar a experiência do usuário.

## ⚙️ Arquitetura

A arquitetura do sistema é baseada em componentes serverless, garantindo escalabilidade e baixo custo operacional. A seguir estão os principais componentes utilizados:

1. Amazon Lex – Interface de Conversação (NLP)

O Amazon Lex é responsável pelo reconhecimento de intenções e entidades nas mensagens do usuário.

Ele ajuda a transformar a linguagem natural em dados estruturados que podem ser processados por funções Lambda.

2. AWS Lambda – Lógica de Negócio

Funções Lambda são acionadas pelas intenções detectadas pelo Lex para realizar ações como:

Consultar informações em bancos de dados.

Interagir com APIs externas.

Gerar respostas dinâmicas utilizando IA generativa (Amazon Bedrock ou OpenAI).

3. Amazon Bedrock (ou OpenAI via API externa) – IA Generativa

A integração com a Amazon Bedrock ou a OpenAI (via API externa) possibilita que o chatbot utilize modelos de IA generativa para responder a perguntas mais complexas ou criar respostas criativas.

4. Amazon DynamoDB – Armazenamento de Sessões e Histórico

O DynamoDB armazena o histórico de conversas e dados temporários das sessões, permitindo que o chatbot "lembre" interações passadas e melhore o contexto das conversas.

5. Amazon API Gateway – Exposição via API

O API Gateway facilita a comunicação entre o front-end (pode ser um site ou aplicativo) e o backend (Lex + Lambda).

6. Amazon Cognito – Autenticação de Usuários

O Cognito é utilizado para gerenciar a autenticação dos usuários, garantindo segurança e controle de acesso.

7. Amazon S3 + CloudFront – Front-End do Bot

A interface do chatbot (caso seja web ou aplicativo) pode ser hospedada no S3, com CloudFront garantindo a entrega rápida e eficiente dos conteúdos.

8. Amazon CloudWatch – Logs e Monitoramento

O CloudWatch é utilizado para monitorar e gerar logs das funções Lambda, interações com o Lex, chamadas ao Bedrock e outros componentes do sistema.

## 🚀 Funcionalidade do Chatbot

Entrada do Usuário: O usuário interage com o chatbot através de uma interface (site, app ou plataforma de mensagens como WhatsApp).

### Processamento da Mensagem:

O texto é enviado ao Amazon Lex, que identifica a intenção do usuário e extrai as informações relevantes.

Se necessário, o AWS Lambda processa essa informação, consulta bases de dados ou chama o Amazon Bedrock para gerar respostas complexas ou criativas.

**Resposta ao Usuário:**

O Lex formata a resposta e envia de volta ao usuário através da interface.

**Armazenamento e Contexto:**

O histórico de interações é salvo no DynamoDB para melhorar o contexto e a experiência em futuras conversas.

## 📦 Tecnologias Utilizadas

- **Amazon Lex** - Serviço de chatbots com NLP (Natural Language Processing)

- **AWS Lambda** - Execução de código serverless

- **Amazon Bedrock (ou OpenAI)** - IA generativa para respostas sofisticadas

- **Amazon DynamoDB** - Banco de dados NoSQL para armazenamento de sessões e histórico

- **Amazon API Gateway** - Gerenciamento de APIs para comunicação entre frontend e backend

- **Amazon S3** - Armazenamento de conteúdo estático

- **Amazon CloudWatch** - Monitoramento e logs


## 🛠️ Melhorias Futuras

**Multi-idioma:** Expansão do chatbot para suportar múltiplos idiomas.

**Análise de Sentimentos:** Utilização do Amazon Comprehend para detectar emoções nas mensagens e ajustar o tom do bot.

**Integração com outras plataformas:** Expansão do bot para integrar com plataformas como Facebook Messenger, WhatsApp ou Slack.

**Reinforço de aprendizagem:** Implementação de técnicas de aprendizado de máquina para melhorar a performance do bot ao longo do tempo.