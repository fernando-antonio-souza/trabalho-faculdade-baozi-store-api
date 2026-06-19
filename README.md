# 🥟 Baozi Store API

![Java](https://img.shields.io/badge/Java-21-orange)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-4.x-green)
![JPA](https://img.shields.io/badge/Spring%20Data-JPA-blue)
![Database](https://img.shields.io/badge/Database-H2-lightgrey)
![Status](https://img.shields.io/badge/Status-Concluído-success)

## 📖 Sobre o Projeto

A Baozi Store API é uma aplicação desenvolvida como atividade prática da disciplina de Desenvolvimento Web Back-End do curso de Engenharia de Software da UNINTER.

O projeto tem como objetivo aplicar conceitos fundamentais do desenvolvimento de APIs REST utilizando o ecossistema Spring, permitindo o gerenciamento de clientes, produtos e pedidos de uma loja fictícia chamada Baozi Store.

---

## 🎯 Objetivos de Aprendizagem

Durante o desenvolvimento deste projeto foram praticados conceitos importantes como:

* Desenvolvimento de APIs REST
* Programação Orientada a Objetos (POO)
* Spring Boot
* Spring Data JPA
* Persistência de dados
* Banco de dados relacional
* Operações CRUD
* Arquitetura em camadas
* Mapeamento de entidades

---

## 🛠️ Tecnologias Utilizadas

### Back-End

* Java 21
* Spring Boot
* Spring Web MVC
* Spring Data JPA

### Banco de Dados

* H2 Database

### Gerenciamento de Dependências

* Maven

---

## 📂 Estrutura do Projeto

```text
src
└── main
    ├── java
    │   └── com.trabalho.baozi_store
    │       ├── controller
    │       │   ├── ClienteController
    │       │   ├── ProdutoController
    │       │   └── PedidoController
    │       │
    │       ├── model
    │       │   ├── Cliente
    │       │   ├── Produto
    │       │   └── Pedido
    │       │
    │       ├── repository
    │       │   ├── ClienteRepository
    │       │   ├── ProdutoRepository
    │       │   └── PedidoRepository
    │       │
    │       └── BaoziStoreApplication
    │
    └── resources
        └── application.properties
```

---

## 🗄️ Modelo de Dados

### Cliente

| Campo        | Tipo      |
| ------------ | --------- |
| id           | Long      |
| nome         | String    |
| clienteDesde | LocalDate |

### Produto

| Campo   | Tipo       |
| ------- | ---------- |
| id      | Long       |
| nome    | String     |
| preco   | BigDecimal |
| estoque | Boolean    |

### Pedido

| Campo      | Tipo    |
| ---------- | ------- |
| id         | Long    |
| clienteId  | Long    |
| produtoId  | Long    |
| quantidade | Integer |

---

## 🔗 Endpoints Disponíveis

### Clientes

| Método | Endpoint       |
| ------ | -------------- |
| POST   | /clientes      |
| GET    | /clientes      |
| GET    | /clientes/{id} |
| DELETE | /clientes/{id} |

---

### Produtos

| Método | Endpoint       |
| ------ | -------------- |
| POST   | /produtos      |
| GET    | /produtos      |
| GET    | /produtos/{id} |
| DELETE | /produtos/{id} |

---

### Pedidos

| Método | Endpoint      |
| ------ | ------------- |
| POST   | /pedidos      |
| GET    | /pedidos      |
| GET    | /pedidos/{id} |
| DELETE | /pedidos/{id} |

---

## 💾 Banco de Dados H2

A aplicação utiliza banco de dados H2 em memória.

Configuração atual:

```properties
spring.datasource.url=jdbc:h2:mem:testdb
spring.jpa.hibernate.ddl-auto=update
spring.h2.console.enabled=true
```

Console H2:

```text
http://localhost:8080/h2-console
```

---

## 🧪 Testando a API

Os endpoints podem ser testados utilizando:

* Postman
* Insomnia
* Thunder Client (VS Code)

Exemplo de criação de cliente:

```json
{
  "nome": "Fernando",
  "clienteDesde": "2026-01-01"
}
```

---

## 📚 Aprendizados

Este projeto permitiu consolidar conhecimentos em:

* Construção de APIs REST com Spring Boot
* Persistência de dados com JPA
* Operações CRUD
* Organização de projetos Java
* Integração entre aplicação e banco de dados
* Boas práticas de desenvolvimento Back-End

---
