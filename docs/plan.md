# Plan: LUMA OS SALON MVP

## Phase 1 — Foundation
### Goal
Establish safe, working app structure and base business model.

### Deliverables
- repo setup and docs
- auth + role-based access
- client model
- professional model
- service model
- business model
- local Docker environment

### Key tasks
1. Set up app environment
2. Configure Prisma schema
3. Configure auth and roles
4. Create client CRUD
5. Create professional CRUD
6. Create service CRUD
7. Add dashboard shell
8. Validate local runs

## Phase 2 — Appointment engine
### Goal
Create schedule and booking flow with validation.

### Deliverables
- agenda view
- appointment creation
- conflict detection
- status updates
- history reading
- reminders hook

### Key tasks
1. Create schedule grid
2. Implement conflict detection
3. Implement appointment creation flow
4. Implement editing/canceling
5. Add status changes
6. Link appointment to client history
7. Add event/webhook trigger for future automation

## Phase 3 — Commission system
### Goal
Track the value of services and professional commissions.

### Deliverables
- commission model
- commission calculation
- audit trail
- dashboard of commissions
- payout-ready data

### Key tasks
1. Define commission rules
2. Implement commission log
3. Connect commission to appointment or order
4. Add dashboard metrics
5. Add audit records
6. Validate calculations with tests

## Phase 4 — Operational dashboard
### Goal
Give reception/management a clear monitor of the business.

### Deliverables
- daily metrics
- appointment list
- no-show indicators
- revenue summary
- professional productivity summary

### Key tasks
1. Dashboard metrics
2. Alert cards
3. Recent activity
4. Professional summary
5. Daily revenue summary

## Phase 5 — Automation layer
### Goal
Prepare data and integrations for future WhatsApp and AI automation.

### Deliverables
- webhook event emitter
- N8N-ready payloads
- reminder templates
- automation triggers

### Key tasks
1. Implement event system
2. Add reminder logic
3. Prepare WhatsApp integration hooks
4. Prepare N8N payloads
5. Validate event logs

## Phase 6 — NF-e groundwork
### Goal
Prepare infrastructure for future invoice issuance.

### Deliverables
- invoice model
- invoice generation hooks
- certificate config placeholders
- audit log
- environment documentation

### Key tasks
1. Design invoice schema
2. Document certificate handling
3. Add secure config placeholders
4. Add invoice generation state machine
5. Prepare compliance notes

## Phase 7 — Production readiness
### Goal
Move from local to secure production.

### Deliverables
- Vercel deployment
- production env
- secure secrets
- monitoring
- backups
- health check

### Key tasks
1. Set production envs
2. Configure secure access
3. Add monitoring
4. Add backups
5. Validate deployment
