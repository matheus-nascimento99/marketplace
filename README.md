# 🛍️ Marketplace

[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)]()
[![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)]()
[![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)]()
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)]()
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)]()

Uma plataforma moderna e robusta para gestão de vendas de produtos, construída com as melhores práticas de desenvolvimento e tecnologias de ponta.

## ✨ Preview

<table>
  <tr>
    <td width="33%">
      🏠 Dashboard
      <img src="/api/placeholder/400/200" alt="Dashboard Preview"/>
    </td>
    <td width="33%">
      📦 Produtos
      <img src="/api/placeholder/400/200" alt="Products Preview"/>
    </td>
    <td width="33%">
      📊 Métricas
      <img src="/api/placeholder/400/200" alt="Metrics Preview"/>
    </td>
  </tr>
</table>

## 🎯 Destaques

- ⚡ **Performance**: Server Components do Next.js para renderização otimizada
- 🛡️ **Segurança**: Autenticação robusta e proteção de dados
- 📱 **Responsivo**: Interface adaptável para todos os dispositivos
- 🧪 **Testável**: Cobertura completa com testes unitários, integração e E2E
- 🎨 **UI/UX**: Componentes modernos com Radix UI
- 📊 **Métricas**: Analytics detalhados de vendas e engajamento

## 🚀 Tecnologias

### Frontend
- Next.js com Server Components
- Radix UI para componentes de interface
- KY e TanStack Query para gerenciamento de requisições HTTP
- TypeScript

### Backend
- NestJS
- PostgreSQL
- Prisma ORM
- TypeScript
- Princípios SOLID e DDD (Domain-Driven Design)
- Testes unitários, de integração e E2E

## 💡 Funcionalidades Principais

### 👤 Gerenciamento de Usuários
  - Cadastro e autenticação segura com hash de senha
  - Atualização de dados com validações
  - Proteção contra duplicidade de e-mail e telefone

### 📦 Gestão de Produtos
  - Criação e edição de produtos
  - Upload de imagens
  - Categorização
  - Sistema de status (Disponível, Vendido, Cancelado)
  - Visualizações de produtos

### 🏷️ Categorias
  - Listagem de categorias disponíveis
  - Acesso público às categorias

### 📊 Métricas e Analytics
  - Produtos vendidos nos últimos 30 dias
  - Produtos disponíveis nos últimos 30 dias
  - Visualizações nos últimos 30 dias
  - Visualizações por dia (últimos 30 dias)
  - Visualizações por produto (últimos 7 dias)

## ⚙️ Configuração do Ambiente

### Pré-requisitos
```markdown
✓ Node.js
✓ Docker
✓ NPM ou Yarn
```

### 🔧 Backend

1. Inicie o container do PostgreSQL:
```bash
docker compose up -d
```

2. Instale as dependências:
```bash
npm install
```

3. Execute as migrações do banco de dados:
```bash
npx prisma migrate deploy
```

4. Inicie o servidor de desenvolvimento:
```bash
npm run start:dev
```

### 🎨 Frontend

1. Instale as dependências:
```bash
npm install
```

2. Inicie o servidor de desenvolvimento:
```bash
npm run dev
```

## 🧪 Testes

```bash
# Testes Unitários e de Integração
npm run test

# Testes E2E
npm run test:e2e
```

## 📚 Regras de Negócio

### 👤 Usuários
- Não é permitido cadastro com e-mail ou telefone duplicado
- Senha armazenada com hash criptográfico
- Atualização de dados com validação de duplicidade

### 📦 Produtos
- Valores armazenados em centavos
- Sistema de status com regras específicas:
  - Produtos vendidos não podem ser editados
  - Produtos cancelados não podem ser marcados como vendidos
  - Produtos vendidos não podem ser cancelados
- Apenas o proprietário pode editar seus produtos
- Sistema de visualizações com proteção contra duplicidade

### 👁️ Visualizações
- Proprietários não podem registrar visualizações em seus próprios produtos
- Proteção contra visualizações duplicadas
- Registro apenas para produtos e usuários existentes