# 🧩 AutBot — Chatbot Inclusivo

> **Apoio, informação e acessibilidade para a comunidade do Transtorno do Espectro Autista.**

![Status](https://img.shields.io/badge/Status-Em_Desenvolvimento-yellow)
![Versão](https://img.shields.io/badge/Versão-2025.2-blue)
![Licença](https://img.shields.io/badge/Licença-MIT-green)

---

## 🧠 Sobre o Projeto

O **AutBot** é uma ferramenta web acessível e empática, desenvolvida para apoiar pais, cuidadores, professores e profissionais da educação que interagem com pessoas com Transtorno do Espectro Autista (TEA).

Nosso objetivo é reduzir barreiras digitais e cognitivas, oferecendo suporte informativo confiável sobre rotinas, direitos e inclusão, tudo através de uma interface clara e rigorosamente adaptada para acessibilidade.

### 🎯 Objetivos
* **Informação Confiável:** Respostas automatizadas baseadas em documentos oficiais (leis, guias, boas práticas).
* **Acessibilidade Cognitiva:** Foco em alto contraste, leitura por voz e navegação facilitada.
* **Segurança:** Conformidade total com a **LGPD**, garantindo tratamento ético dos dados.

---

## ✨ Funcionalidades

### 🚀 Novidades da Versão 2025.2
Neste semestre, o AutBot expandiu de um chatbot informativo para uma plataforma de apoio completa:

* **📅 Agenda Integrada:** Organização de rotinas, horários de medicamentos e terapias, essencial para a previsibilidade no dia a dia.
* **📊 Dashboard do Usuário:** Painel visual para acompanhamento de atividades, histórico resumido e gestão de perfil.
* **🔍 Procura de Profissionais:** Ferramenta de busca para conectar famílias a especialistas (psicólogos, fonoaudiólogos, etc.) recomendados.

### 🧩 Funcionalidades Principais
* **Chatbot Inteligente (LLM):** Base de conhecimento especializada em TEA usando Llama 3.2.
* **Autenticação Segura:** Sistema completo de Login, Cadastro e Recuperação de Senha.
* **Interface Acessível:** Design adaptado para leitores de tela e navegação por teclado.
* **Tratamento de Erros:** Mensagens amigáveis e claras para evitar frustração.

---

## 🛠️ Tecnologias Utilizadas

| Camada | Tecnologia | Versão |
| :--- | :--- | :--- |
| **Frontend** | React.js | `19.1.0` |
| **Backend** | Node.js | `20.19.2` |
| **Framework Web** | Express | `5.1.0` |
| **IA / LLM** | Meta AI (Llama) | `llama-3.2-3b-instruct` |
| **Banco de Dados** | PostgreSQL | `16` (via Docker) |
| **Infraestrutura** | Docker | `25.0.3` |
| **Controle de Versão** | Git / npm | `2.41.0` / `10.8.2` |

---

## 📄 Documentação Técnica

Para uma visão aprofundada da arquitetura, personas e requisitos:

* 📄 **Documentação Completa (PDF):** [Acessar PDF](./api/docs/AutBot_Documentacao_Tecnica.pdf)
* 🖼️ **Protótipos (Figma):** [Ver Protótipos do AutBot](#)

---

## 🔒 Privacidade e LGPD

Levamos a privacidade a sério.
* **Uso de Dados:** Exclusivamente para personalização da experiência e segurança.
* **Controle:** O usuário pode interromper o uso a qualquer momento.
* **Segurança:** As interações são armazenadas de forma segura e não são compartilhadas com terceiros para fins comerciais.

---

## 🚀 Como Executar o Projeto

### Pré-requisitos
* **Node.js** e **npm** instalados.
* **Docker** e **Docker Compose** instalados.
* Chaves de API do [OpenRouter](https://openrouter.ai/) e [Hugging Face](https://huggingface.co/).

### Passo a Passo

#### 1. Clonar o Repositório
```bash
git clone [[https://github.com/accessible-bot/accessible-bot.git](https://github.com/accessible-bot/accessible-bot.git)](https://github.com/App-AutBot/autBot-backend.git)
cd accessible-bot
```
#### 2. Instalar Dependências
```bash
npm install
```


#### 3 . Configurar Variáveis de Ambiente
Crie um arquivo .env na raiz do projeto (baseado no .env.example) e preencha as variáveis:

Snippet de código
```bash
OPENROUTER_API_KEY=sua_chave_aqui
HUGGINGFACE_TOKEN=seu_token_aqui
DB_USER=seu_usuario
DB_PASS=sua_senha
DB_HOST=localhost
DB_PORT=5432
DB_NAME=autbot_db
```

#### 4. Configurar o Banco de Dados (Via Docker)
A maneira mais recomendada de rodar o banco:

```bash

# Subir o container do PostgreSQL
docker-compose up -d
``` 
Caso precise acessar o terminal do banco:
```bash
docker exec -it autbot_postgres bash
# Dentro do container: psql -U <usuario> -d <nome_do_banco>
```
#### 5. Iniciar a Aplicação
```bash
npm start
```
A aplicação estará disponível em: http://localhost:3000

##  🤝 Contribuição
Faça um Fork do projeto.

Crie uma Branch para sua Feature (git checkout -b feature/NovaFeature).

Faça o Commit (git commit -m 'Adicionando nova feature').

Faça o Push (git push origin feature/NovaFeature).

Abra um Pull Request.
