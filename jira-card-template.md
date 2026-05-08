# Template para Refinement

Copie este template, preencha com dados do Jira e cole no chat com o Agent.

---

Card: [CARD-ID]
Title: [Título do card]

Description:
[Descrição completa do card]

Acceptance Criteria:
- [Critério 1]
- [Critério 2]
- [Critério 3]

Additional Context (opcional):
- Priority: [High/Medium/Low]
- Sprint: [Sprint name]
- Related Cards: [Links]
- Technical Notes: [Notas técnicas]

---

## Exemplo Preenchido:

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