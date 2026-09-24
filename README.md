# API de Catálogo Funko Pop - Game of Thrones

API REST para gerenciar um catálogo de Funko Pops de Game of Thrones, com persistência em PostgreSQL.

**Stack:** Node.js, Express, TypeScript, Sequelize, PostgreSQL e pnpm.

Projeto da atividade AT1 de Integração e Entrega Contínua (Docker, GitHub Actions, ESLint, Prettier e Husky).

## Como rodar

Pré-requisito: Docker e Docker Compose.

```bash
cd backend
docker compose up -d --build
docker ps
```

- API: http://localhost:3000
- Documentação (Swagger): http://localhost:3000/api-docs

Para parar:

```bash
docker compose down
```

## Scripts (dentro de `backend/`)

| Comando | Função |
|---|---|
| `pnpm lint` | Análise estática (ESLint) |
| `pnpm format` | Formatação (Prettier) |
| `pnpm typecheck` | Checagem de tipos (`tsc --noEmit`) |
| `pnpm build` | Build de produção |

## Qualidade e CI

- **Husky:** o hook `pre-commit` roda lint e checagem de tipos e bloqueia o commit se houver erro.
- **GitHub Actions:** a cada `push`, o workflow em `.github/workflows/ci.yml` instala as dependências, roda lint, checagem de tipos e build.