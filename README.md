# 🚀 DeliveryTech – API de Delivery

API REST desenvolvida em Spring Boot 3 + Java 21, simulando o backend de uma plataforma de delivery (similar ao iFood e Uber Eats).

Este projeto representa o núcleo do sistema DeliveryTech, contendo camadas bem definidas de Controllers, Services, Repositories e DTOs, além de regras de negócio, validações e transações.

## ℹ️ Contexto do Projeto

Este projeto foi originalmente desenvolvido por mim em uma conta antiga do GitHub, à qual não possuo mais acesso.

Este repositório é um fork, mantido e evoluído na minha conta atual, contendo melhorias, refatorações e atualizações, aplicando boas práticas e conhecimentos adquiridos ao longo da minha evolução como desenvolvedor Back-End Java.

## 🧩 Tecnologias Utilizadas

- ☕ Java 21
- ⚙️ Spring Boot 3.3.5
- 🌐 Spring Web (API REST)
- 💾 Spring Data JPA
- 🧠 ModelMapper (DTO ↔ Entity)
- 🧱 H2 Database (em memória)
- 🧾 Bean Validation
- 🧰 Lombok
- 📦 Maven

## ⚙️ Como Executar o Projeto
### 🔧 Pré-requisitos
- JDK 21
- Maven 3.9+
- IntelliJ IDEA, VS Code ou Spring Tools Suite

### 🚀 Passos para rodar
git clone https://github.com/seuusuario/delivery-api.git
dd delivery-api
mvn spring-boot:run

A aplicação estará disponível em:
👉 [http://localhost:8080](http://localhost:8080)

## 🧠 Estrutura de Pacotes:
**src/main/java/com/deliverytech/delivery**
| **Pacote** | **Descrição** |
| --- | --- |
| `controller` | Endpoints REST |
| `dto` | Objetos de transferência de dados |
| `entity` | Entidades JPA |
| `exception` | Exceções personalizadas |
| `repository` | Interfaces JPA |
| `service` | Regras de negócio e transações |
| `DeliveryApiApplication.java` | Classe principal da aplicação |

## 🌍 Endpoints Principais 
### 🧑‍💼 Cliente 
| Método | Endpoint | Descrição |
| --- | --- | --- |
| POST   | /api/clientes             | Cadastrar cliente |
| GET    | /api/clientes/{id}        | Buscar por ID     |
| GET    | /api/clientes             | Listar clientes   |
| PUT    | /api/clientes/{id}        | Atualizar dados   |
| PATCH  | /api/clientes/{id}/status | Ativar/desativar  |
 
### 🍔 Restaurante 
| Método | Endpoint                                | Descrição             |
| ---    | ---------------------------------------  | ---------------------|
| POST   | /api/restaurantes                       | Cadastrar restaurante|
| GET    | /api/restaurantes/{id}                  | Buscar restaurante     |
| GET    ||/api/restaurantes                       ||Listar disponíveis     ||
similarly for the rest of the endpoints.

# 📦 Pedido

| Método | Endpoint | Descrição |
| ------ | -------------------------- | -------------------- |
| POST   | /api/pedidos               | Criar pedido         |
| GET    | /api/pedidos/{id}          | Buscar pedido        |
| GET    | /api/clientes/{id}/pedidos | Histórico do cliente |
| PATCH  | /api/pedidos/{id}/status   | Atualizar status     |
| DELETE | /api/pedidos/{id}          | Cancelar pedido      |

# 🧪 Exemplos de Requisições

## 🧍‍♂️ Cadastrar Cliente

```http
POST /api/clientes
{
  "nome": "João Silva",
  "email": "joao@email.com",
  "telefone": "11999999999",
  "endereco": "Rua A, 123"
}
```

## 🧾 Criar Pedido

```http
POST /api/pedidos
{
  "clienteId": 1,
  "restauranteId": 1,
  "enderecoEntrega": "Rua B, 456",
  "itens": [
    { "produtoId": 1, "quantidade": 2 },
    { "produtoId": 2, "quantidade": 1 }
  ]
}
```

# 🧰 Banco de Dados H2

**URL:** [http://localhost:8080/h2-console](http://localhost:8080/h2-console),
**JDBC URL:** `jdbc:h2:mem:deliverydb`,
**Usuário:** sa
**Senha:** (em branco)

# 📄 Licença
Projeto desenvolvido para fins educacionais.

# 💙 Desenvolvido por Arthur Lanzoni
