# Blueprint: Security Framework

## Objetivo

Garantir que o sistema seja seguro desde o início, com foco em:

- autenticação por usuário e perfil
- controle de acesso por negócio
- validação de entrada de dados
- auditoria de ações críticas
- proteção contra abuso e ataques comuns

## Regras mínimas

### Autenticação
- Supabase Auth
- login por usuário e senha
- perfil associado a businessId e role
- 2FA como opção em ambiente de produção

### Autorização
- cada usuário só acessa dados do seu negócio
- profissional acessa apenas seus agendamentos
- recepcionista acessa dados da operação geral
- gestor acessa relatórios e comissões

### Validação de entrada
- uso de Zod em todas as actions/forms
- sanitização mínima em todos os inputs
- validação de telefone, e-mail, CPF, datas e horários

### Segurança de dados
- não commitar senhas, tokens ou certs
- armazenar chaves em variáveis de ambiente
- usar Redis para rate limit e cache seguro
- usar criptografia em campos sensíveis, se necessário

### OWASP checklist inicial
- A01 Broken Access Control
- A03 Injection
- A05 Security Misconfiguration
- A07 Identification and Authentication Failures
- A09 Logging and Monitoring Failures

## Medidas recomendadas

- RLS no banco
- middleware de autenticação por rota
- rate limiting para endpoints públicos e sensíveis
- CSRF em formulários
- headers de segurança em produção
- logs de ações críticas
- Sentry e monitoramento de erros

## Ações críticas a auditar

- agendamento criado/alterado/cancelado
- comissão calculada/paga
- cancelamento de cliente ou agendamento
- alteração de dados sensíveis
- MFA / login / sessão
- NFe emitida, rejeitada ou cancelada

## Segurança de produção

- HTTPS obrigatório
- secret manager ou variáveis seguras do ambiente
- backups automatizados
- degradação segura em caso de falha do banco
- monitoramento por alertas e logs
