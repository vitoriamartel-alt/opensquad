---
execution: subagent
agent: squads/proesc-social/agents/daniela-dados
inputFile: squads/proesc-social/output/research-focus.md
outputFile: squads/proesc-social/output/research-report.md
model_tier: powerful
---

# Step 02: Pesquisa de Pautas

## Context Loading

Load these files before executing:
- `squads/proesc-social/output/research-focus.md` — Tema e recorte temporal definido pelo usuário
- `squads/proesc-social/_memory/memories.md` — Histórico de pautas usadas (para evitar repetição)
- `squads/proesc-social/pipeline/data/research-brief.md` — Pilares de conteúdo e landscape competitivo

## Instructions

### Process
1. Ler research-focus.md para extrair o tema específico e o recorte temporal.
2. Executar as tarefas na ordem: `find-news.md` → `rank-stories.md`
3. Salvar o output final (ranked_stories) em `squads/proesc-social/output/research-report.md`

## Output Format

```yaml
research_focus:
  topic: "..."
  time_range: "..."

ranked_stories:
  - rank: 1
    score: X.X
    title: "..."
    source_url: "..."
    core_data: "..."
    angles_preview:
      - emotion: "🔴 Medo"
        hook: "..."
      - emotion: "🟢 Oportunidade"
        hook: "..."
    recommended: true
    recommendation_reason: "..."
  # ... (3-5 stories total)
```

## Output Example

```yaml
research_focus:
  topic: "inadimplência escolar 2025"
  time_range: "Último mês"

ranked_stories:
  - rank: 1
    score: 4.7
    title: "Inadimplência escolar atinge 18,3% no 1T25"
    source_url: "https://estadao.com.br/educacao/inadimplencia-2025"
    core_data: "18,3% de inadimplência em escolas privadas no 1T25 — maior índice desde 2019"
    angles_preview:
      - emotion: "🔴 Medo"
        hook: "Sua escola vai receber só 81% do que é devido esse trimestre."
      - emotion: "🟢 Oportunidade"
        hook: "Enquanto escolas brigam com inadimplência, algumas operam com 5%. O diferencial é um processo."
    recommended: true
    recommendation_reason: "Dado recente e surpreendente com múltiplos ângulos possíveis — máximo potencial"
```

## Veto Conditions

Reject and redo if ANY are true:
1. Menos de 3 pautas no output
2. Alguma pauta sem URL verificável

## Quality Criteria

- [ ] 3-5 pautas ranqueadas com scores
- [ ] Cada pauta tem 2 ângulos preview com hooks
- [ ] Pauta #1 marcada como recommended com justificativa
