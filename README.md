# 📘 API de Estudos em .NET

Este projeto é uma API REST desenvolvida com .NET para fins de aprendizado e experimentação. Ele cobre conceitos como arquitetura em camadas, Entity Framework Core, autenticação básica e uso de containers com Docker.

---

## 🚀 Tecnologias Utilizadas

- [.NET 8](https://dotnet.microsoft.com/)
- [Entity Framework Core](https://learn.microsoft.com/en-us/ef/core/)
- [SQL Server (via Docker)](https://hub.docker.com/_/microsoft-mssql-server)
- [Swagger](https://swagger.io/) para documentação da API
- [Docker](https://www.docker.com/) para ambiente de banco de dados

---

## 📦 Instalação e Execução

### 1. Clone o repositório
```bash
git clone https://github.com/seu-usuario/api-de-estudos.git
cd api-de-estudos

---
### 2. Configure variáveis de ambiente
Crie um arquivo .env com:

Código
DB_PASSWORD=SuaSenhaSegura

### 3. Suba o banco de dados com Docker
```bash
docker run -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=SuaSenhaSegura" \
   -p 1433:1433 --name sqlserver -d mcr.microsoft.com/mssql/server:2022-latest

### 4. Execute a API
```bash
dotnet run
📚 Endpoints Principais
Acesse a documentação interativa via Swagger:

Código
http://localhost:5000/swagger
Exemplos de endpoints:

GET /api/usuarios

POST /api/usuarios

PUT /api/usuarios/{id}

DELETE /api/usuarios/{id}

🧪 Testes
Os testes estão localizados na pasta tests/. Para executá-los:

bash
dotnet test
📌 TODO
[ ] Implementar autenticação JWT

[ ] Criar testes de integração

[ ] Adicionar CI/CD com GitHub Actions