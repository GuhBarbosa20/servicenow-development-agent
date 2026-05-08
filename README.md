# 🤖 ServiceNow Development Agent

Agent de IA especializado em refinement e desenvolvimento ServiceNow.

## 📁 Estrutura do Projeto

```
.
├── .cline/
│   └── custom-instructions.md    # Configuração do agent
├── examples/                     # Exemplos de cards
│   └── example-card-compliance-alert.md
├── refinements/                  # Refinements gerados (auto)
├── jira-card-template.md         # Template para input
├── AGENT-USAGE-GUIDE.md          # Guia completo de uso
└── README.md                     # Este arquivo
```

## 🚀 Quick Start

### 1. Preparar Card do Jira

Copie o template:
```bash
cat jira-card-template.md
```

Preencha com dados do seu card.

### 2. Enviar para o Agent

Cole o card preenchido no chat do Cline.

### 3. Receber Refinement

O agent retorna:
- ✅ Comentário formatado (copiar para Jira)
- ✅ Guia detalhado (salvo em `refinements/`)

## 📖 Documentação

- **Guia Completo**: [AGENT-USAGE-GUIDE.md](AGENT-USAGE-GUIDE.md)
- **Template**: [jira-card-template.md](jira-card-template.md)
- **Exemplo**: [examples/example-card-compliance-alert.md](examples/example-card-compliance-alert.md)

## 🎯 Exemplo Rápido

```
Card: SNOW-456
Title: Implementar monitoramento de compliance score

Description:
Como compliance manager, preciso ser alertado quando o compliance score 
de um control objective cair para zero.

Acceptance Criteria:
- Sistema detecta mudança de score para 0
- Email enviado automaticamente
- Email inclui detalhes do control
```

**Agent retorna:**
- Refinement técnico com 4 tasks
- Guia de implementação completo
- Código pronto para usar
- Estratégia de testes

## ✅ O que o Agent Faz

- 📋 **Analisa** requisitos do card
- 🔧 **Quebra** em tasks técnicas
- 📝 **Cria** guia passo-a-passo
- 💻 **Gera** código completo
- 🧪 **Define** testes
- ✉️ **Formata** comentário para Jira

## 🎓 Para Começar

1. Leia: [AGENT-USAGE-GUIDE.md](AGENT-USAGE-GUIDE.md)
2. Veja exemplo: [examples/example-card-compliance-alert.md](examples/example-card-compliance-alert.md)
3. Use template: [jira-card-template.md](jira-card-template.md)
4. Cole no agent e teste!

## 💡 Dicas

- ✅ Seja específico nos acceptance criteria
- ✅ Inclua contexto técnico
- ✅ Revise o código gerado
- ✅ Teste em ambiente DEV primeiro

## 📞 Suporte

- 📖 Documentação: [AGENT-USAGE-GUIDE.md](AGENT-USAGE-GUIDE.md)
- 💬 Dúvidas: Abra uma issue ou pergunte ao agent

---

**Criado por: Gustavo Barbosa**
**Data: 2026-05-08**