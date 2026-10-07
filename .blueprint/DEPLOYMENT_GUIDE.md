# Blueprint: Deployment Guide

## Objetivo

Estruturar a operação em três fases:

1. local via Docker
2. produção via Vercel
3. escala via VPS / Docker Compose / Nginx

## Fase 1: Docker local

### Requisitos
- Docker
- Docker Compose
- Node.js
- PostgreSQL local ou Supabase

### Arquitetura local

- app web em Next.js
- PostgreSQL em container
- Redis em container
- seed data inicial
- hot reload

### Exemplo de docker-compose.yml

```yaml
services:
  app:
    build: .
    ports:
      - "3000:3000"
    env_file:
      - .env
    depends_on:
      - postgres
      - redis

  postgres:
    image: postgres:16
    environment:
      POSTGRES_DB: luma_salon
      POSTGRES_USER: postgres
      POSTGRES_PASSWORD: postgres
    ports:
      - "5432:5432"
    volumes:
      - pgdata:/var/lib/postgresql/data

  redis:
    image: redis:7
    ports:
      - "6379:6379"

volumes:
  pgdata:
```

## Fase 2: Vercel

- frontend em Vercel
- database em Supabase
- Redis via Upstash ou serviço equivalente
- environment variables na plataforma
- monitoramento por logs e health checks

## Fase 3: VPS

Para um ambiente mais robusto, recomenda-se:

- VPS com Docker Compose
- Nginx como proxy reverso
- PostgreSQL dedicado
- Redis dedicado
- backup automatizado
- observabilidade por logs e alertas

## Health checks

- `/api/health`
- teste de conexão com banco
- teste de Redis
- rotina de fallback para banco primário/backup

## Deploy checklist

- ambiente preparado
- secrets configurados
- RLS disponível
- backups programados
- logs ativos
- monitoramento configurado
