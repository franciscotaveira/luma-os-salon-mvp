# Blueprint: Architecture Overview

## Objetivo da arquitetura

Construir uma base sólida para um sistema de gestão de salão com foco em:

- operação local e remota
- escalabilidade gradual
- segurança por perfil
- automação por eventos e webhooks
- uso em web responsiva e mobile

## Camadas

### 1. Camada de experiência

- Next.js App Router
- UI em componentes reutilizáveis
- responsividade para desktop e celular
- layout operacional para recepcionistas e gestores
- painel para profissionais

### 2. Camada de aplicação

- Server Actions para lógica de app
- API Routes para integrações e webhooks
- validação com Zod
- regras de negócio e cálculo de comissão
- geração de eventos para automação

### 3. Camada de dados

- PostgreSQL via Supabase
- Prisma como ORM
- RLS para isolamento por negócio e perfil
- auditoria de alterações e eventos

### 4. Camada de automação

- Webhooks para N8N
- integrações com WhatsApp/WAHA
- chat IA para atendimento
- automação de lembretes, confirmação e follow-up

### 5. Camada de operação

- Docker local
- Vercel para deploy do MVP
- VPS em escalada posterior
- backups, periodicidade e monitoramento

## Módulos principais

- Auth e ACL
- Clientes
- Profissionais
- Serviços
- Agenda
- Comissões
- Histórico
- Dashboard
- Webhooks e integrações
- NF-e

## Regras de integração

- toda ação crítica gera evento
- eventos são publicados para webhook
- webhooks alimentam N8N/WhatsApp/IA
- toda ação de comissão e nota fiscal precisa ser auditável

## Fluxo principal do MVP

```text
Cliente / Recepção
  -> Agenda / agendamento
  -> validação de conflito
  -> criação da linha de atendimento
  -> comissão calculada
  -> lembrete enviado
  -> cliente confirmado / compareceu / faltou
  -> dados atualizados no histórico
```

## Stack recomendada

- Next.js 15
- TypeScript
- Prisma
- Supabase
- Tailwind CSS
- zod
- react-hook-form
- shadcn/ui
- Redis
- Docker
- N8N
