# AGENTS.md

## Project
LUMA OS SALON MVP

## Mission
Build a salon management system for beauty businesses with:
- multi-professional scheduling
- client profile and history
- service catalog
- operational dashboard
- commission tracking
- future WhatsApp / WAHA / N8N automation
- future NF-e generation
- mobile-first web app
- Docker-based local environment
- deploy strategy for Vercel and VPS

## Core principles
1. Product first, not feature inflation.
2. MVP operational before automation.
3. No secrets in code.
4. Acceptance criteria before implementation.
5. Test before merge.
6. Review is mandatory.
7. Security by design.
8. One task = one objective.
9. Document decisions.
10. Every critical action must be auditable.

## Stack
- Next.js 15 + TypeScript
- Prisma + PostgreSQL
- Supabase Auth + RLS
- Tailwind + shadcn/ui
- Docker + Docker Compose
- Redis
- Optional future: N8N + WAHA + LLM chat

## Team roles
- Product Spec Architect
- Solution Architect
- Backend Engineer
- Frontend Engineer
- Database & Infra Engineer
- QA Engineer
- Security Engineer
- DevOps Engineer
- Finance / NF-e Specialist
- Automation / WhatsApp Specialist

## Lifecycle
Every feature must follow this order:
1. SPEC
2. PLAN
3. IMPLEMENT
4. TEST
5. REVIEW
6. SHIP

## Product focus
Prioritize the core business flow:
- manage professionals
- schedule services
- validate conflicts
- track client history
- calculate commissions
- generate operational insights

## Risk boundaries
Do not build:
- WhatsApp automation before the appointment core works
- NF-e before operational flow is stable
- future modules before MVP is validated
- inventory management before schedule + commissions are proven
- client features before auth and roles are fixed

## Must do
- Check repo state before changes
- Read the relevant files before implementation
- Validate assumptions with evidence
- Write acceptance criteria before coding
- Keep tasks small and reviewable
- Use local Docker for validation
- Document environment variables
- Keep secrets out of source control
- Use webhooks for future automation
- Log critical actions

## Must not do
- Hardcode secrets
- Commit certificates or keys
- Skip tests or verification
- Merge without review
- Assume auth/roles are solved without evidence
- Ignore audit trail for financial actions
- Implement NF-e before the operational core is functional
- Add unrelated modules too early

## Acceptance criteria baseline
- multi-professional schedule works
- conflicts are prevented
- commissions are calculable and traceable
- client history exists
- dashboard operational is visible
- authentication and roles work
- DB RLS is present
- Docker local environment runs

## Required commands
- npm install
- npm run dev
- npm run test
- npm run lint
- docker compose up --build
- npx prisma generate
- npx prisma migrate dev

## Review gate
No task is done until:
- implementation exists
- tests pass
- code is lint-clean
- relevant docs updated
- threat/security review passed
- acceptance criteria validated
- diff reviewed

## Change control
Changes impacting:
- database schema
- auth / roles
- billing / commissions
- NF-e
- integrations
- security
- infra

must be explicitly approved before implementation.

## Escalation
Escalate to a human when:
- legal/compliance risk exists
- customer data exposure risk exists
- NF-e certificate handling is involved
- authentication or authorization unexpectedly fails
- financial calculation errors affect commissions or payouts
- production infrastructure is at risk
