---
task: "Generate Structured Feedback"
order: 2
input:
  - scorecard: Scorecard com notas e issues do score-content.md
  - content_package: Conteúdo avaliado (content-package.md)
output:
  - review_report: Relatório de revisão final com veredito, feedback acionável e instruções de correção se necessário
---

# Generate Structured Feedback

Transforma o scorecard em um relatório de revisão final — com veredito claro, feedback acionável e instruções específicas de correção onde necessário.

## Process

1. **Ler o scorecard** gerado na tarefa anterior.

2. **Consolidar o veredito global**: Se qualquer plataforma tem REVISÃO NECESSÁRIA, o veredito global é REVISÃO NECESSÁRIA. Se todas são APROVADO ou APROVADO COM RESSALVAS, o veredito é o mais baixo entre as plataformas.

3. **Para cada issue_critical**: Gerar instrução de correção específica (o que mudar + como mudar + por quê).

4. **Para cada issue_important**: Gerar sugestão de melhoria com impacto esperado.

5. **Identificar o que foi bem** (top 2-3 pontos positivos por avaliação) — reforçar padrões positivos.

6. **Emitir o veredito final** com próximo passo claro:
   - APROVADO → "Pronto para publicação. Próximo passo: checklist de publicação."
   - APROVADO COM RESSALVAS → "Publicável com ajustes menores. Recomendações abaixo."
   - REVISÃO NECESSÁRIA → "Retornar para Caio Copy com instruções abaixo antes de publicar."

## Output Format

```markdown
# Relatório de Revisão — [Pauta] | [Data]

## 🏆 Veredito Final: [APROVADO | APROVADO COM RESSALVAS | REVISÃO NECESSÁRIA]

**Resumo:** [1-2 frases explicando o veredito de forma direta]

---

## ✅ O que funcionou bem

1. [Ponto positivo específico] — [impacto para engajamento]
2. [Ponto positivo específico] — [impacto]
3. [Ponto positivo específico] — [impacto]

---

## 🔴 Correções obrigatórias (Impacto Crítico)
*[Só aparece se houver issues_critical. Se vazio, remover seção.]*

### [Plataforma] — [Descrição do problema]
**Problema:** [O que está errado]
**Por quê é crítico:** [Impacto na publicação ou credibilidade]
**Ação necessária:** [Instrução específica de correção — o que escrever ou mudar]

---

## 🟡 Melhorias recomendadas (Impacto Importante)
*[Só aparece se houver issues_important. Se vazio, remover seção.]*

### [Plataforma] — [Descrição]
**Situação atual:** [O que está na versão atual]
**Sugestão:** [Como melhorar — específico]
**Impacto esperado:** [Por que essa melhoria importa]

---

## 💡 Sugestões opcionais
*[Só aparece se houver issues_suggestion. Se vazio, remover seção.]*

- [Plataforma]: [Sugestão breve]

---

## 📊 Scorecard Resumido

| Plataforma | Brand Voice | Hook | Valor | CTA | Accuracy | Nota Média | Veredito |
|---|---|---|---|---|---|---|---|
| Instagram | X/10 | X/10 | X/10 | X/10 | ✅/❌ | X.X | APROVADO |
| LinkedIn | ... | ... | ... | ... | ... | ... | ... |
| YouTube | ... | ... | ... | ... | ... | ... | ... |
| Facebook | ... | ... | ... | ... | ... | ... | ... |
| TikTok | ... | ... | ... | ... | ... | ... | ... |

---

## ➡️ Próximo Passo

[Uma instrução clara: "Pronto para publicação — use o checklist de publicação em content-package.md" OU "Retornar para Caio Copy com as correções críticas acima antes de publicar"]
```

## Quality Criteria

- [ ] Veredito final declarado no início (APROVADO / APROVADO COM RESSALVAS / REVISÃO NECESSÁRIA)
- [ ] Seção "O que funcionou bem" presente com ≥ 2 pontos positivos
- [ ] Issues críticos têm "Ação necessária" específica (não "melhore o hook")
- [ ] Scorecard resumido com tabela de notas por plataforma
- [ ] Próximo passo claro e único

## Veto Conditions

Reject and redo if ANY are true:
1. Veredito global não declarado no início do relatório
2. Issue crítico sem instrução específica de correção
