# SKILL: Project Initialization Framework

## Version
1.0 — 2026-10-07

## Objective
Padronizar a estrutura e o protocolo de execução de qualquer projeto novo para que ele seja operável por IAs especializadas, com governança, rastreabilidade, leitura contextual e revisão obrigatória.

## When to use
- novo projeto de software
- novo produto ou solução
- novo cliente ou campanha
- novo processo interno
- qualquer contexto que precise de disciplina e onboarding rápido

## Inputs
- objetivo do projeto
- stack e tecnologias
- equipe envolvida
- restrições e limites
- prazo ou janela de entrega

## Outputs
- AGENTS.md
- LEIA-ME.md
- PROJECT.md
- docs/spec.md
- docs/plan.md
- docs/tasks.md
- docs/review-checklist.md
- prompts por agente
- estrutura de projeto padronizada

## Recommended folder structure

```text
projeto/
├── AGENTS.md
├── LEIA-ME.md
├── PROJECT.md
├── README.md
│
├── docs/
│   ├── spec.md
│   ├── plan.md
│   ├── tasks.md
│   ├── review-checklist.md
│   ├── architecture.md
│   ├── security.md
│   └── MODELOS.md
│
├── prompts/
│   ├── product-spec.md
│   ├── architect.md
│   ├── backend.md
│   ├── frontend.md
│   ├── qa.md
│   ├── security.md
│   ├── devops.md
│   └── finance.md
│
├── src/
│
├── acervo/
│   └── .gitignore
│
├── workflows/
│
├── .gitignore
├── .env.example
└── docker-compose.yml
```

## First-read protocol for AI
When an AI opens the project, it should read this in order:

1. LEIA-ME.md (2 minutes)
2. AGENTS.md (5 minutes)
3. PROJECT.md (10 minutes)
4. docs/spec.md if the task is about what to build
5. docs/plan.md if the task is about how to execute
6. docs/tasks.md if the task is atomic or a sprint item
7. docs/review-checklist.md before marking any task done

Rules:
- never execute scripts without checking their content
- never commit secrets or certificates
- never skip review gates
- never assume requirements without evidence
- never mix code with uncontrolled docs
- never start without the right context

## Standard file properties
Every note or file should include these properties when applicable:

```markdown
---
tipo: [contexto-ia | decisão | spec | plan | task | prompt | skill | processo]
type: [project-context | requirement-spec | execution-plan | atomic-task | instruction-prompt | reusable-skill | procedure]
area: [nome-da-area]
status: [ativo | congelado | concluído | deprecado]
criado: [YYYY-MM-DD]
atualizado: [YYYY-MM-DD]
resumo: "Uma linha descritiva"
proprietario: [nome ou role]
dependências: [arquivo1, arquivo2]
---
```

## Standard AGENTS.md template

```markdown
# AGENTS.md — [Project Name]

## Mission
[Objective in 2-3 lines]

## Core principles
1. [Principle 1]
2. [Principle 2]
3. [Principle 3]

## Team roles
- Product Spec Architect
- Solution Architect
- Backend Engineer
- Frontend Engineer
- QA Engineer
- Security Engineer
- DevOps Engineer

## Lifecycle
1. SPEC
2. PLAN
3. IMPLEMENT
4. TEST
5. REVIEW
6. SHIP

## Must do
- diagnose before prescribing
- use task-based execution
- validate with tests and evidence
- keep docs updated
- avoid secrets in source

## Must not do
- skip review gates
- assume context without checking files
- merge unverified work
- add unrelated scope without approval

## Review gate
No task is done until:
- implementation exists
- tests pass
- docs updated
- security review passed
- acceptance criteria validated
- diff reviewed
```

## Standard LEIA-ME.md template

```markdown
# LEIA-ME — [Project Name]

## Start here
Read in this order:
1. LEIA-ME.md
2. AGENTS.md
3. PROJECT.md
4. docs/spec.md
5. docs/plan.md
6. docs/tasks.md
7. docs/review-checklist.md

## Folder meaning
| Path | Meaning | Permission |
|------|---------|------------|
| /docs | specification and planning | read + update with context |
| /src | source code | implement |
| /prompts | specialist prompts | read + use |
| /acervo | imported material | read only |
| /workflows | automation | read and update when allowed |

## Conduct
- diagnose before prescribing
- prefer simple, verifyable solutions
- do not invent requirements
- keep data local and secure
- avoid secrets in code
- validate before closing work
```

## Validation checklist
A project is ready for IA-driven collaboration when:
- [ ] AGENTS.md exists and is clear
- [ ] LEIA-ME.md exists
- [ ] PROJECT.md exists
- [ ] spec.md exists
- [ ] plan.md exists
- [ ] tasks.md exists
- [ ] review-checklist.md exists
- [ ] prompts folder exists
- [ ] properties pattern is applied
- [ ] .gitignore protects secrets and acervo
- [ ] deployment / local run path is documented

## Use in real life
When a new project starts, do the following:
1. create LEIA-ME.md
2. create AGENTS.md
3. create PROJECT.md
4. create docs folder
5. create prompts folder
6. validate against checklist
7. start implementation

## Versioning
- v1.0: base framework
- v1.1: add team alignment improvements
- v1.2: add automation prompts and review patterns
