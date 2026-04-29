#  Spring Security + JWT — Autenticação de Usuários

![Java](https://img.shields.io/badge/Java-17+-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring%20Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)

> Projeto de estudo focado na implementação de autenticação e autorização com **Spring Security** e **JSON Web Token (JWT)** em uma API REST stateless.

---

##  Índice

- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades](#-funcionalidades)
- [Tecnologias](#-tecnologias)
- [Como Executar](#-como-executar)
- [Endpoints da API](#-endpoints-da-api)
- [Fluxo de Autenticação](#-fluxo-de-autenticação)
- [Estrutura do Projeto](#-estrutura-do-projeto)
- [Aprendizados](#-aprendizados)

---

##  Sobre o Projeto

Este projeto foi desenvolvido com o objetivo de aprender e praticar os conceitos de segurança em aplicações Java com **Spring Security**. A aplicação implementa um fluxo completo de autenticação de usuários utilizando **JWT**, garantindo que os endpoints sejam protegidos e acessíveis apenas por usuários autenticados.

---

##  Funcionalidades

- [x] Cadastro de usuário
- [x] Login com geração de token JWT
- [x] Validação do token em requisições protegidas
- [x] Proteção de endpoints por autenticação
- [x] API stateless (sem sessões no servidor)

---

##  Tecnologias

| Tecnologia       | Versão  |
|------------------|---------|
| Java             | 17+     |
| Spring Boot      | 3.x     |
| Spring Security  | 6.x     |
| JWT (jjwt)       | 0.12.x  |
| Spring Data JPA  | —       |
| H2 / PostgreSQL  | —       |
| Maven            | —       |

---

##  Como Executar

### Pré-requisitos

- Java 17+
- Maven instalado

### Passo a passo

```bash
# Clone o repositório
git clone https://github.com/AllanGabriel03/SpringSecurity.git

# Entre na pasta do projeto
cd SpringSecurity

# Execute a aplicação
./mvnw spring-boot:run
```

A aplicação estará disponível em: `http://localhost:8080`

---

##  Endpoints da API

###  Públicos (não requerem autenticação)

| Método | Endpoint          | Descrição              |
|--------|-------------------|------------------------|
| POST   | `/auth/register`  | Cadastro de usuário    |
| POST   | `/auth/login`     | Login e geração do JWT |

###  Protegidos (requerem Bearer Token)

| Método | Endpoint   | Descrição                        |
|--------|------------|----------------------------------|
| GET    | `/users/me` | Retorna dados do usuário logado |


---

##  Aprendizados

Durante o desenvolvimento deste projeto, foram explorados os seguintes conceitos:

- **Cadeia de filtros do Spring Security** — como as requisições são interceptadas e processadas
- **Autenticação vs. Autorização** — diferença entre validar quem o usuário é e o que ele pode fazer
- **JWT (JSON Web Token)** — estrutura, assinatura e validação de tokens
- **Stateless API** — eliminação de sessões no servidor com o uso de tokens
- **`UserDetailsService`** — como o Spring carrega os dados do usuário durante a autenticação
- **`SecurityFilterChain`** — configuração moderna do Spring Security 6

---

##  Contato

Desenvolvido por **Allan Gabriel**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/allangabriel03/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AllanGabriel03)
