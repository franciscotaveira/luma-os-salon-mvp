# Tasks: LUMA OS SALON MVP

## Task 1 — Repo setup and docs baseline
**Owner:** Project lead / architect
**Status:** Pending
**Goal:** Create a clean project skeleton and shared execution context.

**Acceptance criteria**
- [ ] repo exists and is understandable
- [ ] AGENTS.md is present
- [ ] docs/spec.md exists
- [ ] docs/plan.md exists
- [ ] docs/tasks.md exists
- [ ] initial README exists

**Dependencies**
- none

**Verification**
- repo directory structure reviewed
- docs present and consistent

---

## Task 2 — Local Docker environment
**Owner:** DevOps Engineer
**Status:** Pending
**Goal:** Make the app run locally with Docker.

**Acceptance criteria**
- [ ] docker-compose.yml runs locally
- [ ] app container starts
- [ ] postgres starts
- [ ] redis starts
- [ ] health endpoint works

**Dependencies**
- Task 1

**Verification**
- `docker compose up --build`
- `docker compose ps`

---

## Task 3 — Prisma schema foundation
**Owner:** Backend Engineer + DB Engineer
**Status:** Pending
**Goal:** Define the core data model.

**Acceptance criteria**
- [ ] Business model exists
- [ ] Client model exists
- [ ] Professional model exists
- [ ] Service model exists
- [ ] Appointment model exists
- [ ] Commission model exists
- [ ] ClientHistory exists

**Dependencies**
- Task 1

**Verification**
- `npx prisma validate`
- `npx prisma generate`

---

## Task 4 — Auth and role-based access
**Owner:** Backend Engineer + Security Engineer
**Status:** Pending
**Goal:** Protect routes and data by role.

**Acceptance criteria**
- [ ] login works
- [ ] user has role and business association
- [ ] admin can access business-level resources
- [ ] professional sees only their schedule
- [ ] receptionist sees business-wide operations

**Dependencies**
- Task 2
- Task 3

**Verification**
- auth flow test
- role policy test
- RLS test

---

## Task 5 — Client management
**Owner:** Backend + Frontend
**Status:** Pending
**Goal:** Allow registration and management of clients.

**Acceptance criteria**
- [ ] client list displays
- [ ] client create works
- [ ] client edit works
- [ ] client profile has history
- [ ] validation prevents bad data

**Dependencies**
- Task 4

**Verification**
- unit test for client schema
- integration test for CRUD

---

## Task 6 — Professional management
**Owner:** Backend + Frontend
**Status:** Pending
**Goal:** Manage professionals and service assignment.

**Acceptance criteria**
- [ ] professional list displays
- [ ] create professional works
- [ ] service assignment works
- [ ] commission rate stored
- [ ] working hours stored

**Dependencies**
- Task 4

**Verification**
- CRUD validation test
- profile creation flow test

---

## Task 7 — Service catalog
**Owner:** Backend + Frontend
**Status:** Pending
**Goal:** Maintain available salon services.

**Acceptance criteria**
- [ ] services display
- [ ] duration and price stored
- [ ] service has availability by professional
- [ ] service editing works

**Dependencies**
- Task 4

**Verification**
- service validation tests
- CRUD test

---

## Task 8 — Schedule grid
**Owner:** Frontend Engineer
**Status:** Pending
**Goal:** Show daily schedule by professional.

**Acceptance criteria**
- [ ] grid renders correctly
- [ ] each professional has a column
- [ ] time slots display
- [ ] appointments are visible on the grid

**Dependencies**
- Task 5
- Task 6
- Task 7

**Verification**
- UI component test
- schedule snapshot review

---

## Task 9 — Appointment creation
**Owner:** Backend + Frontend
**Status:** Pending
**Goal:** Create real bookings with conflict validation.

**Acceptance criteria**
- [ ] appointment can be created
- [ ] conflict detection blocks double booking
- [ ] validation errors are clear
- [ ] appointment is stored with correct status

**Dependencies**
- Task 8

**Verification**
- unit test for conflict detection
- integration test for booking creation

---

## Task 10 — Appointment status flow
**Owner:** Backend + Frontend
**Status:** Pending
**Goal:** Manage booking state changes.

**Acceptance criteria**
- [ ] scheduled becomes confirmed/in progress/completed
- [ ] cancellations update history
- [ ] statuses are auditable

**Dependencies**
- Task 9

**Verification**
- status-based tests
- event log validation

---

## Task 11 — Client history
**Owner:** Backend + Frontend
**Status:** Pending
**Goal:** Keep a complete client attendance history.

**Acceptance criteria**
- [ ] appointment completion updates client history
- [ ] professional/service appear in history
- [ ] notes and feedback captured
- [ ] history displays in client profile

**Dependencies**
- Task 9
- Task 10

**Verification**
- history CRUD test
- profile test

---

## Task 12 — Commission engine
**Owner:** Finance / Backend Engineer
**Status:** Pending
**Goal:** Compute professional commissions.

**Acceptance criteria**
- [ ] commission rule is applied
- [ ] commission log is created
- [ ] audit info exists
- [ ] dashboard uses commission data

**Dependencies**
- Task 9

**Verification**
- commission calculation tests
- financial calculation checks

---

## Task 13 — Dashboard operational
**Owner:** Frontend + Backend
**Status:** Pending
**Goal:** Show relevant business metrics for the day.

**Acceptance criteria**
- [ ] revenue summary appears
- [ ] appointments count appears
- [ ] no-show indicators appear
- [ ] professional productivity appears

**Dependencies**
- Task 9
- Task 12

**Verification**
- dashboard snapshot tests
- data correctness validation

---

## Task 14 — Webhooks and automation hooks
**Owner:** Automation Specialist + Backend
**Status:** Pending
**Goal:** Prepare points for future automation.

**Acceptance criteria**
- [ ] appointment created event fires
- [ ] appointment updated event fires
- [ ] event log is stored
- [ ] payload is N8N-ready

**Dependencies**
- Task 9

**Verification**
- webhook test
- event payload validation

---

## Task 15 — NF-e groundwork
**Owner:** Finance / NF-e Specialist
**Status:** Pending
**Goal:** Prepare invoice foundations without forcing full production early.

**Acceptance criteria**
- [ ] invoice model exists
- [ ] invoice generation state exists
- [ ] certificate setup is documented
- [ ] environment config is protected

**Dependencies**
- Task 12

**Verification**
- model validation
- secure config review

---

## Task 16 — Security and review
**Owner:** Security Engineer
**Status:** Pending
**Goal:** Validate production-readiness of base system.

**Acceptance criteria**
- [ ] RLS review complete
- [ ] role isolation validated
- [ ] secrets not committed
- [ ] rate limiting considered
- [ ] logs and audit trail reviewed

**Dependencies**
- all major tasks

**Verification**
- security checklist review
- penetration-style review of critical paths

---

## Task 17 — Production deployment prep
**Owner:** DevOps Engineer
**Status:** Pending
**Goal:** Prepare the app to deploy safely.

**Acceptance criteria**
- [ ] env examples are complete
- [ ] Docker runs successfully
- [ ] Vercel config exists
- [ ] health checks are present
- [ ] backup policy is defined

**Dependencies**
- all previous tasks

**Verification**
- deploy dry-run
- health check endpoint validation
