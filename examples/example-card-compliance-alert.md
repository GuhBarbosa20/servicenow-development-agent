# Exemplo de Card - Compliance Score Alert

Este é um exemplo de card do Jira formatado para o agent.

---

Card: SNOW-456
Title: Implementar monitoramento de compliance score

Description:
Como compliance manager, preciso ser alertado quando o compliance score de um control objective cair para zero, para que eu possa investigar e tomar ações corretivas imediatamente.

O sistema deve detectar automaticamente quando o score muda de qualquer valor para zero e enviar notificação por email.

Acceptance Criteria:
- Sistema detecta mudança de score para 0 em tempo real
- Email enviado automaticamente para compliance.manager@ibm.com
- Email inclui: nome do control, score anterior, link para o control
- Não enviar múltiplos emails para o mesmo evento
- Registrar alerta em tabela de histórico

Additional Context:
- Priority: High
- Sprint: Sprint 23
- Related Cards: SNOW-123 (Integration monitoring)
- Technical Notes: Usar Business Rule, não Scheduled Job

---

## Como usar este exemplo:

1. Copie o conteúdo acima (do "Card:" até o final do Additional Context)
2. Cole no chat com o agent
3. Aguarde o refinement completo
4. Copie o comentário gerado para o Jira
5. Consulte o arquivo detalhado em refinements/