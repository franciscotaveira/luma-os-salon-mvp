# LUMA OS SALON MVP

Sistema operacional de gestão para salão de beleza com agenda, agendamento, comissionamento de profissionais, histórico de clientes e base pronta para WhatsApp/Chat AI + NF-e.

## Objetivo

Criar um MVP funcional para uso real em salão de beleza com múltiplos profissionais, focado em:

- agenda operacional
- agendamento pela recepção
- cliente com histórico e preferências
- comissionamento por profissional
- lembretes automáticos
- base para automação com WhatsApp/WAHA, N8N e IA
- preparação para emissão de NF-e

## Arquitetura inicial

- Frontend: Next.js 15 + TypeScript + Tailwind
- Backend: Next.js App Router + Server Actions / API Routes
- Banco: PostgreSQL via Supabase
- ORM: Prisma
- Autenticação: Supabase Auth + RLS
- Infra: Docker local + Vercel + VPS em fase seguinte
- Mensageria: Webhooks + N8N

## Roadmap

### Fase 1 - MVP operacional (30 dias)
- login e autenticação por perfil
- clientes
- profissionais
- serviços
- agenda visual
- agendamento com validação de conflito
- comissões por profissional
- dashboard operacional
- histórico do cliente
- lembretes básicos

### Fase 2 - Automação de atendimento
- WhatsApp / WAHA
- chat sales com IA
- confirmação por WhatsApp
- lembretes 24h / 2h
- automações via N8N

### Fase 3 - NF-e e operação financeira
- emissão de NF-e com certificado digital
- faturamento e auditoria
- relatórios de comissões
- gestão de movimentação financeira

## Estrutura planejada

```text
app/
blueprint/
components/
actions/
lib/
prisma/
public/
Dockerfile
docker-compose.yml
.env.example
README.md
```

## Comandos iniciais

```bash
docker compose up --build
```

```bash
npm install
npm run dev
```

## Boas práticas já consideradas

- autenticação por role
- RLS no banco
- validação com Zod
- rate limiting
- csrf em formulários
- logs e auditoria
- webhooks para automação
- backups e monitoramento

## Observações

Este repositório é a base do MVP, pensado para evoluir para WhatsApp/Chat AI, automação N8N e emissão de NF-e sem quebrar a estrutura operacional do agendamento.
