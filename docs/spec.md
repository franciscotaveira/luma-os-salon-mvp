# Spec: LUMA OS SALON MVP

## Objective
Create an operational salon management system for a beauty business with multiple professionals, focused on core business execution before automation.

## Core business
The system must support:
- appointment scheduling for multiple professionals
- client registration and history
- professional registration and service assignment
- service catalog with prices, duration and commission rules
- dashboard for daily operations
- commission calculation
- attendance and follow-up states
- future automation via WhatsApp / N8N / AI

## Primary users
- receptionist
- manager
- professional
- client (future public booking flow)

## Success definition
The business can operate with:
- scheduling without overlap for the same professional
- visibility of agenda by day and professional
- customer history and preferences
- commission calculation for each professional
- basic dashboard metrics
- reliable local environment

## Acceptance criteria
- [ ] A receptionist can create a client
- [ ] A receptionist can create a professional
- [ ] A receptionist can create a service
- [ ] A professional has a defined schedule
- [ ] A user can create an appointment without time conflict
- [ ] A conflicting appointment is rejected
- [ ] A completed appointment updates the client history
- [ ] Commission is calculated and stored with audit data
- [ ] Dashboard shows daily operational metrics
- [ ] Auth roles restrict access by role and business
- [ ] Local Docker environment runs successfully

## Scope boundaries
### In scope
- appointment scheduling
- client profile
- professional profile
- service setup
- commission logic
- dashboard
- authentication and roles
- local infra
- future webhook/event layer

### Out of scope (for now)
- full e-commerce
- online payment processing
- advanced inventory
- full NF-e automation
- WhatsApp AI automation
- advanced analytics
- multi-business expansion beyond base structure

## MVP vs future roadmap
### MVP
- operational scheduling
- client management
- professional management
- service catalog
- commission tracking
- dashboard
- secure role-based access

### Future
- public booking page
- WhatsApp automation
- AI sales/chat
- N8N workflows
- NF-e automation
- inventory
- advanced campaigns and CRM

## Risks
- confusion between multi-brand and multi-professional logic
- commission calculation errors
- scheduling conflict bugs
- data leak between roles
- inconsistent business segmentation

## Decisions
- Operational flow comes before automation
- Commission modeling is core business logic
- Security and access control are non-negotiable
- Local Docker is mandatory for development
- Default deployment path: Vercel for web app, VPS later for scale
