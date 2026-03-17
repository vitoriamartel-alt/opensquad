---
task: "Rank Stories for Content"
order: 2
input:
  - raw_sources: Lista de 5-8 fontes de find-news.md
  - squad_memory: Histórico de pautas usadas (memories.md)
output:
  - ranked_report: 3-5 pautas ranqueadas com análise e ângulo potencial
---

# Rank Stories for Content

Transforma as fontes brutas em pautas ranqueadas por potencial de engajamento, prontas para o checkpoint de seleção do usuário.

## Process

1. **Ler as fontes** do output da tarefa anterior (find-news.md) e o squad memory para verificar pautas já usadas.

2. **Avaliar cada fonte** em 3 dimensões:
   - **Relevância** (1-5): Quão diretamente impacta o dia a dia de gestores escolares da Proesc?
   - **Ângulo potencial** (1-5): Quantos ângulos emocionais distintos essa pauta permite?
   - **Dados de suporte** (1-5): Quão bom é o dado central? Específico, recente, surpreendente?

3. **Calcular score** de cada fonte: média das 3 dimensões. Ranquear do maior para o menor score.

4. **Eliminar pautas duplicadas** com histórico recente de squad memory.

5. **Escrever 1-2 ângulos potenciais** para cada pauta ranqueada — mostra ao usuário o potencial criativo antes da seleção.

6. **Limitar saída a 3-5 pautas** — nunca mais do que 5 no output final.

## Output Format

```yaml
ranked_stories:
  - rank: 1
    score: 4.7
    dimensions:
      relevance: 5
      angle_potential: 5
      data_quality: 4
    title: "Título da pauta"
    source_url: "..."
    source_date: "YYYY-MM-DD"
    core_data: "Dado principal em 1 frase"
    angles_preview:
      - emotion: "🔴 Medo"
        hook: "Primeira linha proposta para esse ângulo"
      - emotion: "🟢 Oportunidade"
        hook: "Primeira linha alternativa"
    recommended: true | false
    recommendation_reason: "Por que essa pauta tem o maior potencial"
```

## Output Example

```yaml
ranked_stories:
  - rank: 1
    score: 4.7
    dimensions:
      relevance: 5
      angle_potential: 5
      data_quality: 4
    title: "Inadimplência escolar bate 18,3% no 1T25 — maior índice desde 2019"
    source_url: "https://www.estadao.com.br/educacao/inadimplencia-escolar-2025"
    source_date: "2025-03-12"
    core_data: "18,3% de inadimplência média em escolas privadas no 1T25, alta de 2,1pp vs 1T24"
    angles_preview:
      - emotion: "🔴 Medo"
        hook: "Sua escola está entre os 18% que não vão receber o que é devido esse trimestre."
      - emotion: "🟢 Oportunidade"
        hook: "Enquanto escolas brigam com inadimplência, algumas reduziram para 4%. Veja como."
    recommended: true
    recommendation_reason: "Dado recente e surpreendente + dor universal para todos os gestores + múltiplos ângulos emocionais possíveis"
  - rank: 2
    score: 4.0
    dimensions:
      relevance: 4
      angle_potential: 4
      data_quality: 4
    title: "MEC lança plataforma de gestão para escolas públicas"
    source_url: "https://mec.gov.br/plataforma-gestao-2025"
    source_date: "2025-03-08"
    core_data: "Plataforma gratuita para gestão acadêmica em escolas públicas, com 50K inscrições em 72h"
    angles_preview:
      - emotion: "📚 Educacional"
        hook: "O que a iniciativa do MEC revela sobre o futuro da gestão escolar no Brasil"
      - emotion: "↔️ Contrário"
        hook: "O governo digitalizou a escola pública. E as escolas privadas ainda usam planilha."
    recommended: false
    recommendation_reason: "Relevante mas foco em escola pública pode não converter bem para o ICP da Proesc (privadas)"
```

## Quality Criteria

- [ ] Entre 3 e 5 pautas no output (não mais, não menos)
- [ ] Score calculado com 3 dimensões explícitas para cada pauta
- [ ] Pauta #1 tem recommended: true com razão específica
- [ ] Cada pauta tem pelo menos 2 ângulos potenciais com hooks
- [ ] Nenhuma pauta está no histórico recente de memories.md

## Veto Conditions

Reject and redo if ANY are true:
1. Mais de 5 pautas no output — excede o limite do checkpoint de seleção
2. Pauta #1 não tem recommended: true declarado
