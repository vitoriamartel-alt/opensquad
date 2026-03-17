---
execution: inline
agent: squads/proesc-social/agents/estela-estrategia
inputFile: squads/proesc-social/output/selected-story.md
outputFile: squads/proesc-social/output/angles.md
---

# Step 04: Geração de Ângulos

## Context Loading

Load these files before executing:
- `squads/proesc-social/output/selected-story.md` — Pauta selecionada pelo usuário
- `squads/proesc-social/pipeline/data/domain-framework.md` — Content pillars e tipos de hooks
- `squads/proesc-social/pipeline/data/research-brief.md` — Landscape competitivo e audience insights

## Instructions

### Process
1. Ler a pauta selecionada em selected-story.md — extrair título, dado central e fonte.
2. Executar a tarefa `generate-angles.md`: gerar 5 ângulos emocionalmente distintos para a pauta.
3. Para cada ângulo: classificar emoção, escrever hook, definir estrutura narrativa 3 partes, indicar plataforma ideal.
4. Recomendar 1 ângulo com justificativa.
5. Salvar em angles.md.

## Output Format

```yaml
pauta: "..."
core_data: "..."

angles:
  - id: medo
    emotion: "🔴 Medo"
    hook: "..."
    narrative:
      abertura: "..."
      desenvolvimento: "..."
      fechamento: "..."
    platform_ideal: "Instagram"
    format_suggested: "carrossel"

  # ... (5 ângulos total)

recommendation:
  angle_id: "..."
  reason: "..."
```

## Output Example

Exemplo completo disponível em: `squads/proesc-social/pipeline/data/output-examples.md`

## Veto Conditions

Reject and redo if ANY are true:
1. Menos de 5 ângulos gerados
2. Algum ângulo muda a pauta (fala de outro assunto)

## Quality Criteria

- [ ] Exatamente 5 ângulos, um por emoção obrigatória
- [ ] Cada ângulo tem hook + narrativa + plataforma
- [ ] Recomendação explícita com justificativa
