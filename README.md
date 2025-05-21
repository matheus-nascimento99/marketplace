
# 🛍️ Marketplace

[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)]()  
[![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)]()  
[![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)]()  
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)]()  
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)]()  

Uma plataforma moderna e robusta para gestão de vendas de produtos, construída com tecnologias de ponta e boas práticas de desenvolvimento.

---

## ✨ Preview

<table>
  <tr>
    <td width="33%">
      🏠 Dashboard
    </td>
    <td width="33%">
      📦 Produtos  
    </td>
    <td width="33%">
      📊 Métricas  
    </td>
  </tr>
</table>

---

## 🎯 Destaques

- ⚡ **Performance**: Server Components do Next.js para renderização otimizada  
- 🛡️ **Segurança**: Autenticação robusta e proteção de dados  
- 📱 **Responsivo**: Interface adaptável para todos os dispositivos  
- 🧪 **Testável**: Cobertura completa com testes unitários, integração e E2E  
- 🎨 **UI/UX**: Componentes modernos com Radix UI  
- 📊 **Métricas**: Analytics detalhados de vendas e engajamento  

---

## 🚀 Tecnologias

### Frontend

- Next.js com Server Components  
- Radix UI  
- TanStack Query e KY  
- TypeScript  

### Backend

- NestJS  
- PostgreSQL  
- Prisma ORM  
- TypeScript  
- Princípios SOLID e DDD  
- Testes unitários, de integração e E2E  

### Mobile

- React Native  
- Expo  
- TypeScript  

---

## 📱 Aplicativo Mobile

O aplicativo mobile do Marketplace oferece uma experiência intuitiva e eficiente para os usuários gerenciarem suas vendas e compras diretamente de seus dispositivos móveis. Desenvolvido com React Native e Expo, o app permite:

- Visualizar e gerenciar produtos disponíveis
- Acompanhar métricas de vendas e engajamento
- Realizar autenticação segura
- Navegar por categorias e detalhes dos produtos

Com uma interface responsiva e amigável, o aplicativo visa proporcionar praticidade e agilidade no gerenciamento das atividades do Marketplace.

---

## 💡 Funcionalidades Principais

### 👤 Gerenciamento de Usuários

- Cadastro e autenticação segura com hash de senha  
- Atualização de dados com validações  
- Prevenção de duplicidade de e-mail e telefone  

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

---

## ⚙️ Configuração do Ambiente

### Pré-requisitos

```bash
✓ Node.js  
✓ Docker  
✓ NPM ou Yarn  
```

---

### 🔧 Backend

```bash
# Inicie o container do PostgreSQL
docker compose up -d

# Instale as dependências
npm install

# Execute as migrações do banco de dados
npx prisma migrate deploy

# Popule a tabela de categorias com dados iniciais
npx prisma db seed

# Inicie o servidor de desenvolvimento
npm run start:dev
```

---

### 🎨 Frontend

```bash
# Instale as dependências
npm install

# Inicie o servidor de desenvolvimento
npm run dev
```

---

### 📱 Mobile

```bash
# Instale o Expo CLI
npm install -g expo-cli

# Acesse a pasta do projeto mobile
cd marketplace-mobile

# Instale as dependências
npm install

# Inicie o app mobile com Expo
npx expo start
```

---

## 🧪 Testes

```bash
# Testes unitários e de integração
npm run test

# Testes E2E
npm run test:e2e
```

---

## 📚 Regras de Negócio

### 👤 Usuários

- Não é permitido cadastro com e-mail ou telefone duplicado  
- Senha armazenada com hash criptográfico  
- Atualização de dados com validação de duplicidade  

### 📦 Produtos

- Valores armazenados em centavos  
- Regras de status:  
  - Produtos vendidos não podem ser editados  
  - Produtos cancelados não podem ser marcados como vendidos  
  - Produtos vendidos não podem ser cancelados  
- Apenas o proprietário pode editar seus produtos  
- Sistema de visualizações com proteção contra duplicidade  

### 👁️ Visualizações

- Proprietários não podem registrar visualizações em seus próprios produtos  
- Proteção contra visualizações duplicadas  
- Registro apenas para produtos e usuários existentes  

---

## 🔐 Ambiente

> ✅ **Certifique-se de preencher corretamente os arquivos `.env` em todos os projetos (`api`, `web` e `mobile`) para garantir o funcionamento completo da aplicação.**
