<div align="center">

# 💰 Family Budget API

### REST API para Controle de Orçamento Familiar

<img src="https://user-images.githubusercontent.com/104053775/198865741-d76b7df2-613c-4fbb-9d0e-63d4deff540a.jpg" alt="REST API" width="800">

<br>

<p>
  <img src="https://img.shields.io/badge/Java-17-ED8B00?style=flat&logo=openjdk&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/Spring_Boot-2.7.5-6DB33F?style=flat&logo=spring-boot&logoColor=white" alt="Spring Boot">
  <img src="https://img.shields.io/badge/MySQL-8.0.30-4479A1?style=flat&logo=mysql&logoColor=white" alt="MySQL">
  <img src="https://img.shields.io/badge/Docker-Ready-2496ED?style=flat&logo=docker&logoColor=white" alt="Docker">
</p>

</div>

***

## 📖 Sobre o Projeto

Meu primeiro projeto de uma API REST desenvolvida para controle de **orçamento familiar**. A aplicação permite que uma pessoa cadastre suas receitas e despesas do mês, bem como gerar um relatório mensal completo com totais por categoria.

### ✨ Funcionalidades

- 🔐 Sistema de autenticação JWT seguro
- 💵 Gerenciamento completo de receitas (CRUD)
- 💳 Gerenciamento completo de despesas (CRUD)
- 📊 Geração automática de relatórios mensais
- 🔍 Filtros por descrição e período
- 📝 Documentação interativa com Swagger
- 🐳 Totalmente dockerizado para fácil deploy

***

## 🚀 Endpoints da API

### Autenticação

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| `POST` | `/register` | Cadastrar usuário para começar a usar a API |
| `POST` | `/auth` | Autenticar usuário e receber token JWT |

### Receitas

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| `GET` | `/receitas` | Listar todas as receitas |
| `GET` | `/receitas/{id}` | Buscar receita por ID |
| `GET` | `/receitas?descricao={valor}` | Buscar receitas por descrição |
| `GET` | `/receitas/{ano}/{mes}` | Listar receitas de um período específico |
| `POST` | `/receitas` | Cadastrar nova receita |
| `PUT` | `/receitas/{id}` | Atualizar receita existente |
| `DELETE` | `/receitas/{id}` | Remover receita |

### Despesas

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| `GET` | `/despesas` | Listar todas as despesas |
| `GET` | `/despesas/{id}` | Buscar despesa por ID |
| `GET` | `/despesas?descricao={valor}` | Buscar despesas por descrição |
| `GET` | `/despesas/{ano}/{mes}` | Listar despesas de um período específico |
| `POST` | `/despesas` | Cadastrar nova despesa |
| `PUT` | `/despesas/{id}` | Atualizar despesa existente |
| `DELETE` | `/despesas/{id}` | Remover despesa |

### Relatórios

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| `GET` | `/resumo/{ano}/{mes}` | Gerar resumo mensal completo |

***

## 📚 Documentação Completa

A API está com o **Swagger2** implementado. Para ver a **documentação interativa completa**, rode a aplicação e acesse:

```
http://localhost:8080/swagger-ui.html
```

## 🖼️ Screenshots

<div align="center">

### Docker Rodando
<img src="https://github.com/user-attachments/assets/39a5556d-3bb8-4593-8189-ca01b9a3bf62" alt="Docker Containers" width="800">

### Swagger UI
<img src="https://github.com/user-attachments/assets/c4a034cc-50aa-4924-9783-eb7f688927b1" alt="Swagger" width="800">

### Testando com Insomnia
<img src="https://github.com/user-attachments/assets/cdbfb529-9627-4e13-89e6-fc6203901e21" alt="Insomnia" width="800">

</div>

***

## 🛠️ Tecnologias Utilizadas

### Backend & Framework
- **Java 17** - Linguagem de programação moderna e performática
- **Spring Boot 2.7.5** - Framework para desenvolvimento rápido de aplicações
- **Spring Security 5.7** - Autenticação e autorização robustas
  - 🔄 **Atualização importante:** Projeto utiliza a nova configuração de segurança (Spring Security 5.7+), substituindo o `WebSecurityConfigurerAdapter` deprecated por `SecurityFilterChain` com `@Bean` ([documentação oficial](https://spring.io/blog/2022/02/21/spring-security-without-the-websecurityconfigureradapter))
- **Spring Data JPA** - Camada de persistência simplificada
- **Hibernate** - ORM para mapeamento objeto-relacional
- **Bean Validation** - Validação automática de dados com anotações
- **Arquitetura REST** - Padrão RESTful para APIs escaláveis

### Banco de Dados
- **MySQL 8.0.30** - Sistema de gerenciamento de banco de dados relacional

### Segurança
- **JWT (Json Web Token)** - Autenticação stateless e segura
- **BCrypt** - Algoritmo de hash para senhas

### Documentação & Testes
- **Swagger 2** - Documentação interativa e automática da API
- **JUnit 4** - Framework para testes unitários
- **Mockito** - Framework para criação de mocks em testes

### DevOps & Ferramentas
- **Docker** - Containerização da aplicação
- **Docker Compose** - Orquestração de múltiplos containers
- **Maven** - Gerenciamento de dependências e build
- **Eclipse IDE** - Ambiente de desenvolvimento integrado
- **Insomnia** - Cliente para testes de APIs REST

## 🚀 Como Executar Localmente

### Pré-requisitos

Antes de começar, certifique-se de ter instalado:

- [Docker](https://www.docker.com/get-started) e [Docker Compose](https://docs.docker.com/compose/install/)
- **OU** (se não usar Docker):
  - [Java 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
  - [Maven 3.8+](https://maven.apache.org/download.cgi)
  - [MySQL 8.0.30](https://dev.mysql.com/downloads/mysql/)

### Opção 1: Usando Docker Compose (Recomendado) 🐳

# Clone o repositório
```bash
git clone https://github.com/Rafael-Bessa/family-budget-api.git
```
# Entre na pasta do projeto
```bash
cd family-budget-api
```
# Suba os containers (MySQL + API)
```bash
docker-compose up --build
```
# Aguarde a mensagem: "Started Application in X seconds"

# Acesse: 
```
http://localhost:8080/swagger-ui.html
```



