# 🐳 DevOps Docker Templates

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![NGINX](https://img.shields.io/badge/NGINX-009639?style=for-the-badge&logo=nginx&logoColor=white)

Production-ready Docker Compose templates with CI/CD pipelines.

## Stacks
| Stack | Services | Port |
|-------|----------|------|
| `node-mongo` | Node.js + MongoDB | 3000 |
| `django-postgres` | Django + PostgreSQL | 8000 |
| `nginx-proxy` | NGINX reverse proxy | 80 |

## Quick Start
```bash
# Run a specific stack
cd node-mongo && docker compose up -d

# Run everything
docker compose up -d
```

## CI/CD
Includes GitHub Actions workflow for:
- Dockerfile linting with Hadolint
- Multi-stack parallel builds

## Project Structure
```
devops-docker-templates/
├── node-mongo/
│   ├── Dockerfile
│   └── docker-compose.yml
├── django-postgres/
│   ├── Dockerfile
│   └── docker-compose.yml
├── nginx-proxy/
│   ├── docker-compose.yml
│   └── nginx.conf
├── .github/workflows/ci.yml
├── docker-compose.yml
└── README.md
```
