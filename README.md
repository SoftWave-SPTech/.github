# SoftWave - Organização

<div align="center">
  <h3>Sistema de Gestão Jurídica Completo</h3>
  <p>Desenvolvido pela equipe SoftWave para o escritório Lauriano & Leão Sociedade de Advogados</p>
</div>

---

## 📖 Sobre o Projeto

A **SoftWave** é uma organização dedicada ao desenvolvimento de uma solução completa de gestão jurídica, criada especialmente para o escritório **Lauriano & Leão Sociedade de Advogados**. O projeto consiste em um sistema web moderno e escalável que abrange desde a gestão de clientes e processos até a integração com inteligência artificial para auxílio jurídico.

## 🎯 Objetivo

Criar uma plataforma integrada que permita advogados e clientes gerenciar processos jurídicos, documentos, acompanhar o status de casos, além de oferecer recursos inovadores como:

- Gestão completa de clientes (pessoa física e jurídica)
- Controle de processos e documentos
- Autenticação segura e envio de e-mails automatizados
- Integração com IA (Gemini) para assistência jurídica
- Interface intuitiva e responsiva
- Infraestrutura robusta e escalável

## 🏗️ Arquitetura do Projeto

O projeto está dividido em múltiplos repositórios especializados, seguindo os princípios de microsserviços e separação de responsabilidades:

```
SoftWave-SPTech/
├── backend-softwave       # Backend principal (API REST)
├── react-front-end-repo   # Frontend em React
├── API-GEMINI-IA          # Integração com IA do Gemini
├── API-AUTH-MAIL          # Autenticação e envio de e-mails
├── softwave-infra         # Infraestrutura e DevOps
└── .github                # Configurações da organização
```

---

## 📦 Repositórios

### 1. [backend-softwave](https://github.com/SoftWave-SPTech/backend-softwave)

**Descrição:** Backend principal do sistema, desenvolvido em Java com Spring Boot.

**Funcionalidades:**
- Gerenciamento de usuários (clientes e advogados)
- Processamento de dados em tempo real
- API RESTful completa
- Autenticação e autorização seguras
- Integração com banco de dados MySQL
- Documentação com Swagger

**Tecnologias:**
- Java 21
- Spring Boot (Data JPA, Security)
- MySQL
- Maven
- JUnit (testes)
- Swagger (documentação)

**Como usar:**
```bash
git clone https://github.com/SoftWave-SPTech/backend-softwave.git
cd backend-softwave
mvn clean install
mvn spring-boot:run
```

---

### 2. [react-front-end-repo](https://github.com/SoftWave-SPTech/react-front-end-repo)

**Descrição:** Interface web moderna e responsiva desenvolvida em React com Vite.

**Funcionalidades:**
- Login e autenticação diferenciada (clientes e advogados)
- Cadastro de usuários (PF e PJ)
- Dashboard personalizado por tipo de usuário
- Gestão de documentos e processos
- Upload e visualização de arquivos
- Edição de perfil
- Página institucional
- Catálogo de vídeos e podcast

**Tecnologias:**
- React 18
- Vite
- TailwindCSS
- Axios
- React Router DOM
- SwiperJS
- React Icons

**Como usar:**
```bash
git clone https://github.com/SoftWave-SPTech/react-front-end-repo.git
cd react-front-end-repo
npm install
npm run dev
```
Acesse em: `http://localhost:5173`

---

### 3. [API-GEMINI-IA](https://github.com/SoftWave-SPTech/API-GEMINI-IA)

**Descrição:** Microserviço de integração com a API do Google Gemini AI para assistência jurídica inteligente.

**Funcionalidades:**
- Integração com Gemini AI
- Análise de documentos jurídicos
- Assistência automatizada
- Geração de insights baseados em IA

**Tecnologias:**
- Spring Boot
- Google Gemini API
- Java

**Objetivo:** Fornecer recursos de inteligência artificial para auxiliar advogados na análise de casos e documentos.

---

### 4. [API-AUTH-MAIL](https://github.com/SoftWave-SPTech/API-AUTH-MAIL)

**Descrição:** Microserviço especializado em autenticação de usuários e envio de e-mails.

**Funcionalidades:**
- Autenticação JWT
- Envio de e-mails transacionais
- Recuperação de senha
- Notificações por e-mail
- Gestão de tokens

**Objetivo:** Centralizar a lógica de autenticação e comunicação por e-mail, permitindo que outros serviços se concentrem em suas responsabilidades principais.

---

### 5. [softwave-infra](https://github.com/SoftWave-SPTech/softwave-infra)

**Descrição:** Repositório dedicado à infraestrutura, DevOps e orquestração de containers.

**Conteúdo:**
- Docker e Docker Compose
- Scripts de automação (Shell)
- Configurações de Nginx
- Templates para deploy em nuvem (AWS, Azure, GCP)
- Scripts SQL de inicialização
- Configurações de ambientes

**Tecnologias:**
- Docker
- Docker Compose
- Shell Scripts
- Nginx
- PostgreSQL
- Redis

**Como usar:**
```bash
git clone https://github.com/SoftWave-SPTech/softwave-infra.git
cd softwave-infra
./init.sh        # Inicializa o ambiente
./start.sh       # Inicia todos os serviços
```

**Ambientes suportados:**
- Local (Docker Compose)
- AWS (ECS, CloudFormation)
- Azure (Container Instances, ARM Templates)
- GCP (Cloud Run, Deployment Manager)

---

## 🛠️ Stack Tecnológica

### Backend
- **Java 21** - Linguagem principal
- **Spring Boot** - Framework backend
- **Spring Data JPA** - Persistência de dados
- **MySQL** - Banco de dados relacional
- **PostgreSQL** - Banco alternativo (infra)
- **Redis** - Cache e sessões
- **Maven** - Gerenciador de dependências

### Frontend
- **React 18** - Framework JavaScript
- **Vite** - Build tool e dev server
- **TailwindCSS** - Framework CSS
- **Axios** - Cliente HTTP
- **React Router** - Roteamento

### DevOps & Infraestrutura
- **Docker** - Containerização
- **Docker Compose** - Orquestração local
- **Nginx** - Proxy reverso e load balancer
- **Shell Scripts** - Automação
- **Cloud Platforms** - AWS, Azure, GCP

### Inteligência Artificial
- **Google Gemini AI** - Assistência jurídica inteligente

---

## 🚀 Como Executar o Projeto Completo

### Pré-requisitos
- Docker e Docker Compose instalados
- Git
- Node.js 18+ (para desenvolvimento frontend)
- Java 21+ (para desenvolvimento backend)

### Opção 1: Usando Docker (Recomendado)

```bash
# 1. Clone o repositório de infraestrutura
git clone https://github.com/SoftWave-SPTech/softwave-infra.git
cd softwave-infra

# 2. Inicialize o ambiente
./init.sh

# 3. Configure as variáveis de ambiente
nano .env

# 4. Inicie todos os serviços
./start.sh

# Acesse:
# - Frontend: http://localhost:3000
# - Backend: http://localhost:8080
# - Documentação API: http://localhost:8080/swagger-ui.html
```

### Opção 2: Desenvolvimento Local

**Backend:**
```bash
git clone https://github.com/SoftWave-SPTech/backend-softwave.git
cd backend-softwave
mvn spring-boot:run
```

**Frontend:**
```bash
git clone https://github.com/SoftWave-SPTech/react-front-end-repo.git
cd react-front-end-repo
npm install
npm run dev
```

---

## 📋 Roadmap

- [x] Backend principal com Spring Boot
- [x] Frontend em React com Vite
- [x] Integração com IA (Gemini)
- [x] Sistema de autenticação e e-mail
- [x] Infraestrutura Docker
- [ ] Deploy em produção
- [ ] Testes automatizados completos
- [ ] CI/CD com GitHub Actions
- [ ] Monitoramento e observabilidade
- [ ] App mobile (futuro)

---

## 👥 Equipe SoftWave

Projeto desenvolvido pela equipe **SoftWave-SPTech** para a disciplina de Projetos Integrados da SPTech.

---

## 📄 Licença

Este projeto é de uso exclusivo do escritório **Lauriano & Leão Sociedade de Advogados**.

---

## 📞 Contato

- **Email:** suporte.softwave@gmail.com
- **GitHub:** [@SoftWave-SPTech](https://github.com/SoftWave-SPTech)

---

<div align="center">
  <p>Desenvolvido com ❤️ pela equipe SoftWave</p>
</div>