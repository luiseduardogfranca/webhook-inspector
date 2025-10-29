# Webhook Inspector

Uma aplicação para capturar e inspecionar requisições de webhook, composta por uma API backend e uma interface web frontend.

## 🚀 Tecnologias Principais

### Backend (API)
- **Fastify** - Framework web rápido e eficiente
- **TypeScript** - Linguagem de programação tipada
- **PostgreSQL** - Banco de dados relacional
- **Drizzle ORM** - ORM para TypeScript
- **Zod** - Validação de schemas
- **Docker** - Containerização do banco de dados

### Frontend (Web)
- **React 19** - Biblioteca para interface de usuário
- **Vite** - Build tool e servidor de desenvolvimento
- **TypeScript** - Linguagem de programação tipada

### Ferramentas
- **pnpm** - Gerenciador de pacotes
- **Biome** - Linter e formatador de código
- **Docker Compose** - Orquestração de containers

## 📦 Instalação

### Pré-requisitos
- Node.js (versão 18 ou superior)
- pnpm
- Docker e Docker Compose

### Passos de Instalação

1. **Clone o repositório**
   ```bash
   git clone <url-do-repositorio>
   cd webhook-inspector
   ```

2. **Instale as dependências**
   ```bash
   pnpm install
   ```

3. **Configure o banco de dados**
   ```bash
   cd api
   docker-compose up -d
   ```

4. **Execute as migrações do banco**
   ```bash
   pnpm db:migrate
   ```

5. **Inicie os serviços**

   **Backend (API):**
   ```bash
   cd api
   pnpm dev
   ```

   **Frontend (Web):**
   ```bash
   cd web
   pnpm dev
   ```

## 🌐 Acessos

- **API**: http://localhost:3333
- **Documentação da API**: http://localhost:3333/docs
- **Frontend**: http://localhost:5173

## 📁 Estrutura do Projeto

```
webhook-inspector/
├── api/                 # Backend (Fastify + TypeScript)
├── web/                 # Frontend (React + Vite)
├── package.json         # Configuração do workspace
└── pnpm-workspace.yaml  # Configuração do pnpm workspace
```

## 🛠️ Scripts Disponíveis

### API
- `pnpm dev` - Inicia o servidor de desenvolvimento
- `pnpm db:generate` - Gera migrações do banco
- `pnpm db:migrate` - Executa migrações
- `pnpm db:studio` - Abre o Drizzle Studio

### Web
- `pnpm dev` - Inicia o servidor de desenvolvimento
- `pnpm build` - Gera build de produção
- `pnpm preview` - Visualiza o build de produção
