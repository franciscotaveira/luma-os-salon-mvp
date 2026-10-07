# Sprint 1 - Autenticação e base operacional

## Objetivo

Criar a base da aplicação com autenticação por perfil, clientes e serviços.

## Entregáveis

- login e logout
- roles: admin, recepcionista, profissional
- clientes cadastrados
- profissionais cadastrados
- serviços configurados
- layout operacional por perfil

## Tarefas

1. Setup de auth com Supabase
2. RLS por role e business
3. cadastro de cliente
4. cadastro de profissional
5. cadastro de serviços
6. dashboard inicial por perfil

## Critérios de aceite

- usuário não autorizado não acessa rota
- recepcionista vê operação completa
- profissional vê apenas seu calendário
- cadastro de cliente salva corretamente
- não há conflitos de acesso entre marcas e unidades
