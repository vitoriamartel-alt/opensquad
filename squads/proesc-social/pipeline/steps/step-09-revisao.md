---
execution: inline
agent: squads/proesc-social/agents/renata-revisao
inputFile: squads/proesc-social/output/content-package.md
outputFile: squads/proesc-social/output/review-report.md
on_reject: step-06-criacao.md
---

# Step 09: Revisão de Qualidade

## Context Loading

Load these files before executing:
- `squads/proesc-social/output/content-package.md` — Pacote de conteúdo consolidado
- `squads/proesc-social/pipeline/data/quality-criteria.md` — Critérios de avaliação
- `squads/proesc-social/pipeline/data/anti-patterns.md` — Anti-padrões a verificar
- `squads/proesc-social/pipeline/data/research-brief.md` — Para verificação factual

## Instructions

### Process
1. Ler o content-package.md completo.
2. Executar `score-content.md`: pontuar cada plataforma em todos os critérios universais e específicos.
3. Executar `generate-feedback.md`: transformar scorecard em relatório com veredito, pontos positivos e feedback acionável.
4. Se veredito = REVISÃO NECESSÁRIA: incluir instruções específicas de correção para cada issue crítico.
5. Salvar review-report.md.

**Se veredito = REVISÃO NECESSÁRIA**: Pipeline Runner retorna para step-06 (Caio Copy) com as instruções de correção do review-report.md como inputFile adicional.

## Output Format

Seguir formato exato de `generate-feedback.md`:
- Veredito global no início
- Seção "O que funcionou bem"
- Correções obrigatórias (se houver)
- Melhorias recomendadas (se houver)
- Scorecard resumido em tabela
- Próximo passo

## Veto Conditions

Reject and redo if ANY are true:
1. Veredito global não declarado
2. Issue crítico sem instrução de correção

## Quality Criteria

- [ ] Todas as 5 plataformas com scorecard
- [ ] Veredito global declarado
- [ ] Feedback acionável para issues encontrados
- [ ] Próximo passo claro
