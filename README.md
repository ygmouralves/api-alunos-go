# API REST — Go + Gin + Docker

> API REST de gerenciamento de alunos construída com Go, Gin, GORM e PostgreSQL, containerizada com Docker Compose.

## Endpoints

| Método | Rota | Descrição |
|--------|------|-----------|
| GET | `/alunos` | Lista todos os alunos |
| GET | `/alunos/:id` | Busca aluno por ID |
| POST | `/alunos` | Cria novo aluno |
| PUT | `/alunos/:id` | Atualiza aluno |
| DELETE | `/alunos/:id` | Remove aluno |
| GET | `/:nome` | Rota de saudação |

## Stack

<img src="https://skillicons.dev/icons?i=go,docker,postgres,linux&perline=4"/>

| Tecnologia | Uso |
|-----------|-----|
| Go 1.15+ | Linguagem principal |
| Gin | HTTP framework |
| GORM | ORM para PostgreSQL |
| Docker Compose | Ambiente containerizado |
| validator.v2 | Validação de campos (CPF, RG) |

## Como rodar

```bash
# Subir ambiente com Docker
docker-compose up -d

# Rodar a API
go run main.go

# Rodar os testes
go test ./...
```

## Validações

O model `Aluno` valida:
- `nome`: obrigatório (non-zero)
- `rg`: 9 dígitos numéricos
- `cpf`: 11 dígitos numéricos

---

Desenvolvido com Go · Gin · GORM · PostgreSQL · Docker