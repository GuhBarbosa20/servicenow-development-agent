# 🚀 Como Executar o ServiceNow Development Agent

## Pré-requisitos

1. **VS Code** instalado
2. **Extensão Cline** instalada no VS Code
   - Acesse: https://marketplace.visualstudio.com/items?itemName=saoudrizwan.claude-dev
   - Ou busque "Cline" no marketplace do VS Code

## Passo a Passo Completo

### 1️⃣ Clonar o Repositório

```bash
# Clone o repositório
git clone https://github.com/GuhBarbosa20/servicenow-development-agent.git

# Entre no diretório
cd servicenow-development-agent
```

### 2️⃣ Abrir no VS Code

```bash
# Abra o diretório no VS Code
code .
```

Ou:
- Abra o VS Code manualmente
- File → Open Folder
- Selecione a pasta `servicenow-development-agent`

### 3️⃣ Ativar o Agent (Cline)

1. **Abra o Cline** no VS Code:
   - Clique no ícone do Cline na barra lateral (ícone de robô)
   - Ou use o atalho: `Cmd+Shift+P` → digite "Cline: Open"

2. **Configure a API Key** (primeira vez):
   - O Cline pedirá uma API key da Anthropic (Claude)
   - Acesse: https://console.anthropic.com/settings/keys
   - Crie uma nova API key
   - Cole no Cline

3. **Verifique a configuração**:
   - O Cline carrega automaticamente o arquivo `.cline/custom-instructions.md`
   - Você verá "Bob" como o nome do agent
   - Pronto! O agent está ativo

### 4️⃣ Usar o Agent

#### Opção A: Copiar Template

1. Abra o arquivo `jira-card-template.md`
2. Copie o conteúdo
3. Preencha com dados do seu card Jira
4. Cole no chat do Cline
5. Aguarde a resposta (30-60 segundos)

#### Opção B: Digitar Diretamente

No chat do Cline, digite:

```
Card ID: SNOW-123
Title: Criar notificação de compliance
Description: Enviar email quando score for zero
Acceptance Criteria:
- Email enviado automaticamente
- Template customizável
- Log de envios
```

### 5️⃣ Receber e Usar a Resposta

O agent retorna **2 coisas**:

#### 1. Comentário para Jira (no chat)
```
═══════════════════════════════════════
🤖 TECHNICAL REFINEMENT
═══════════════════════════════════════
[Resumo técnico formatado]
```

**Ação**: Copie e cole como comentário no card do Jira

#### 2. Arquivo Detalhado (salvo automaticamente)
```
refinements/refinement-SNOW-123.md
```

**Ação**: 
- Abra o arquivo no VS Code
- Leia o guia completo de implementação
- Siga os passos para desenvolver

### 6️⃣ Implementar no ServiceNow

1. Abra o arquivo de refinement gerado
2. Siga cada task passo-a-passo
3. Copie o código fornecido
4. Implemente no ServiceNow
5. Execute os testes sugeridos

## Exemplo Prático

### Input (você cola no Cline):
```
Card ID: SNOW-456
Title: Alerta de Compliance Score Zero
Description: Criar notificação automática quando compliance score for zero
Acceptance Criteria:
- Email enviado quando score = 0
- Template de email customizável
- Log de notificações enviadas
```

### Output (agent gera):

**No chat:**
```
═══════════════════════════════════════
🤖 TECHNICAL REFINEMENT - SNOW-456
═══════════════════════════════════════

📋 TASKS BREAKDOWN
1. [3h] Criar Business Rule para detectar score zero
2. [2h] Criar Email Notification template
3. [2h] Criar tabela de log
4. [1h] Testes e validação

⏱️ TOTAL ESTIMATE: 8 horas
🎯 COMPLEXITY: Média
```

**Arquivo gerado:**
```
refinements/refinement-SNOW-456.md (40+ páginas)
```

Contém:
- Análise técnica completa
- Código de cada componente
- Instruções passo-a-passo
- Casos de teste
- Checklist de validação

## Comandos Úteis

### Pedir Mudanças
```
Agent, mude o email template para incluir link do control
```

### Pedir Explicação
```
Agent, explique como funciona o Business Rule que você criou
```

### Pedir Código Adicional
```
Agent, crie também um Script Include para reutilizar essa lógica
```

### Reportar Erro
```
Agent, o código deu erro: [cole o erro aqui]
```

## Dicas de Uso

### ✅ Faça
- Seja específico nos acceptance criteria
- Inclua contexto técnico se tiver
- Revise o código gerado
- Teste em ambiente DEV primeiro
- Peça ajustes se necessário

### ❌ Evite
- Cards muito vagos
- Múltiplos requisitos não relacionados
- Implementar sem revisar o código
- Pular os testes sugeridos

## Troubleshooting

### Problema: Cline não carrega o agent
**Solução**: 
- Verifique se está na pasta correta (deve ter `.cline/` dentro)
- Reabra o VS Code
- Verifique se a extensão Cline está ativa

### Problema: Agent não responde como esperado
**Solução**:
- Verifique se usou o template correto
- Inclua mais detalhes no card
- Tente reformular a pergunta

### Problema: Código gerado não funciona
**Solução**:
- Cole o erro no chat do Cline
- Peça ajuda: "Agent, corrija este erro: [erro]"
- O agent ajustará o código

## Estrutura do Projeto

```
servicenow-development-agent/
├── .cline/
│   └── custom-instructions.md    # ⚙️ Configuração do agent
├── jira-card-template.md         # 📝 Template de input
├── AGENT-USAGE-GUIDE.md          # 📖 Guia de uso
├── COMO-EXECUTAR-AGENT.md        # 🚀 Este arquivo
├── examples/                     # 💡 Exemplos
│   └── example-card-compliance-alert.md
└── refinements/                  # 📁 Refinements gerados
    └── refinement-SNOW-456.md
```

## Vídeo Tutorial

🎥 **Em breve**: Vídeo demonstrando o uso completo do agent

## Suporte

- 💬 **Slack**: #servicenow-agent
- 📧 **Email**: gustavo.barbosa@company.com
- 🐛 **Issues**: https://github.com/GuhBarbosa20/servicenow-development-agent/issues

## Próximos Passos

1. ✅ Clone o repositório
2. ✅ Abra no VS Code
3. ✅ Instale o Cline
4. ✅ Configure a API key
5. ✅ Cole seu primeiro card
6. ✅ Receba o refinement
7. ✅ Implemente no ServiceNow

---

**Criado por: Gustavo Barbosa**
**Última atualização: 2026-05-08**