# 🤖 Guia de Uso - ServiceNow Development Agent

## O que é?

Um AI agent que transforma cards do Jira em:
- ✅ Refinement técnico completo
- ✅ Guias de implementação passo-a-passo
- ✅ Código pronto para usar
- ✅ Estratégia de testes

## Como Usar

### Passo 1: Preparar Input

1. Abra o card no Jira
2. Copie o template: `jira-card-template.md`
3. Preencha com dados do card:
   - Card ID
   - Title
   - Description
   - Acceptance Criteria

### Passo 2: Enviar para o Agent

1. Abra o VS Code com Cline
2. Cole o template preenchido no chat
3. Aguarde resposta (30-60 segundos)

### Passo 3: Usar a Resposta

O Agent retorna 2 coisas:

#### 1. Comentário para Jira (no chat)
```
═══════════════════════════════════════
🤖 TECHNICAL REFINEMENT
═══════════════════════════════════════
[Resumo formatado]
```

**Ação**: Copie e cole como comentário no Jira

#### 2. Arquivo Detalhado (salvo localmente)
```
refinements/refinement-SNOW-456.md
```

**Ação**: Abra e leia o guia completo de implementação

### Passo 4: Implementar

Siga o guia passo-a-passo:
- Cada task tem instruções detalhadas
- Código completo incluído
- Testes especificados
- Checklist de validação

## Exemplos de Uso

### Exemplo 1: Novo Feature
```
Card: SNOW-100
Title: Criar dashboard de compliance
Description: Dashboard mostrando score de todos os controls
Acceptance Criteria:
- Mostrar lista de controls com scores
- Gráfico de tendência
- Filtros por categoria
```

**Agent retorna:**
- 5 tasks técnicas
- Guia de 40 páginas
- Código completo
- 15 test cases

### Exemplo 2: Bug Fix
```
Card: SNOW-101
Title: Corrigir erro na integração AccessHub
Description: Integração falhando com HTTP 500
Acceptance Criteria:
- Identificar causa raiz
- Implementar fix
- Adicionar error handling
```

**Agent retorna:**
- Análise do problema
- 3 tasks de correção
- Código atualizado
- Testes de regressão

### Exemplo 3: Technical Debt
```
Card: SNOW-102
Title: Refatorar Script Include de integração
Description: Código difícil de manter, sem testes
Acceptance Criteria:
- Modularizar código
- Adicionar testes unitários
- Documentar funções
```

**Agent retorna:**
- Plano de refatoração
- Código refatorado
- Suite de testes
- Documentação

## Dicas

### ✅ Boas Práticas

1. **Seja específico** nos acceptance criteria
2. **Inclua contexto** técnico se tiver
3. **Mencione dependências** de outros cards
4. **Revise o código** gerado antes de usar
5. **Teste em DEV** primeiro

### ❌ Evite

1. Cards muito vagos ("melhorar sistema")
2. Múltiplos requisitos não relacionados
3. Falta de acceptance criteria
4. Não revisar o código gerado

## Perguntas Frequentes

**Q: O Agent pode acessar o ServiceNow?**
A: Não, ele apenas gera código. Você implementa manualmente.

**Q: E se o código não funcionar?**
A: Cole o erro no chat e peça ajuda ao Agent.

**Q: Posso pedir mudanças no código?**
A: Sim! "Agent, mude X para Y no código acima"

**Q: Quanto tempo economiza?**
A: Refinement: 2-3 horas → 2 minutos
   Implementação: Guia completo pronto

**Q: Funciona para qualquer tipo de card?**
A: Sim! Features, bugs, tech debt, spikes.

## Estrutura de Arquivos

```
.
├── .cline/
│   └── custom-instructions.md    # Configuração do agent
├── jira-card-template.md         # Template para input
├── AGENT-USAGE-GUIDE.md          # Este arquivo
├── examples/                     # Exemplos de refinements
└── refinements/                  # Refinements gerados
    └── refinement-SNOW-XXX.md
```

## Suporte

- 💬 Canal Slack: #agent-help
- 📧 Email: dev-team@company.com
- 📖 Docs: Consulte este arquivo

## Contribuindo

Encontrou um caso de uso útil? Adicione ao `examples/`!

```bash
git add examples/refinement-SNOW-XXX.md
git commit -m "Add example for [use case]"
git push
```

---

**Criado por: Gustavo Barbosa**
**Última atualização: 2026-05-08**