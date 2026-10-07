# Blueprint: Project Vision

## Visão do produto

O LUMA OS SALON é um sistema operacional para gestão de salão de beleza com múltiplos profissionais.

Ele deve funcionar como um sistema de operação real para recepcionistas, gestores e profissionais, com:

- agenda visual por profissional
- agendamento por dia e horário
- histórico do cliente
- comissionamento proporcional por profissional
- dashboard operacional
- base para atendimento por WhatsApp e IA
- emissão de NF-e em evolução

## Problema central

Muitos negócios de estética e beleza ainda dependem de cadernos, WhatsApp e planilhas. Isso gera:

- perda de agendamentos
- conflitos de horários
- dificuldade de controle de comissão
- ausência de dados históricos
- baixa rastreabilidade
- retrabalho administrativo

## Objetivo do MVP

Entregar um sistema funcional onde:

- a recepção consegue agendar rapidamente
- o gestor consegue ver o que está acontecendo no dia
- o profissional consegue ter visão do seu calendário
- o cliente tem ligação direta com o histórico e com o agendamento
- o negócio consegue controlar comissões e reduzir perdas

## Diferenciais

- operação multi-profissional
- lógica de pagamento de comissão
- base pronta para chat sales + WhatsApp
- prontidão para automação com N8N
- visão para expansão para outras marcas ou unidades

## Escopo MVP

### Obrigatório
- autenticação por perfil
- clientes
- profissionais
- serviços
- agenda visual
- agendamento com validação
- comissões
- dashboard operacional
- histórico do cliente
- notificações básicas

### Futuro
- agenda online para o cliente
- WhatsApp / WAHA
- chat AI + agente de vendas
- NF-e automática
- estoque
- relatórios financeiros avançados

## Regras de negócio principais

1. Um agendamento deve estar vinculado a cliente, serviço e profissional.
2. Não pode haver sobreposição de horário para o mesmo profissional.
3. Cada agendamento pode gerar comissão para o profissional.
4. Comissão deve ser rastreável por regra, status e auditoria.
5. O cliente deve possuir histórico e preferências.
6. O sistema precisa ser operacional sem depender de pagamentos externos no MVP.
