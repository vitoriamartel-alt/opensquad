---
execution: inline
agent: squads/proesc-social/agents/ana-automacao
inputFile: squads/proesc-social/output/content-approved.md
outputFile: squads/proesc-social/output/content-package.md
---

# Step 08: Consolidação e Empacotamento

## Context Loading

Load these files before executing:
- `squads/proesc-social/output/content-approved.md` — Conteúdo aprovado pelo usuário
- `squads/proesc-social/_memory/memories.md` — Histórico de hashtags e pautas anteriores
- `squads/proesc-social/pipeline/data/domain-framework.md` — Calendário editorial e timing de publicação

## Instructions

### Process
1. Ler o conteúdo aprovado em content-approved.md.
2. Executar `consolidate-output.md`: separar por plataforma, gerar checklist de publicação, sugerir timing, sinalizar pending_visual/pending_produção.
3. Gerar conjuntos de hashtags rotacionados (diferentes dos últimos 2 runs em memories.md).
4. Atualizar memories.md com: pauta, ângulo, tom, data e hashtags usados.
5. Salvar pacote em content-package.md.

## Output Format

Seguir formato exato de `consolidate-output.md` task file:
- Seção por plataforma com status, conteúdo e checklist
- Timing de publicação por plataforma
- Pending_visual sinalizados
- Squad memory update registrado

## Veto Conditions

Reject and redo if ANY are true:
1. Alguma das 5 plataformas sem seção no pacote
2. Memories.md não atualizado

## Quality Criteria

- [ ] 5 seções de plataforma com status declarado
- [ ] Checklist de publicação completo por plataforma
- [ ] Timing sugerido para cada plataforma
- [ ] Memories.md atualizado
