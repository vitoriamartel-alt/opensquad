---
task: "Find News & Sources"
order: 1
input:
  - research_focus: Tema e recorte temporal definidos pelo usuário no checkpoint anterior (research-focus.md)
  - content_pillars: Pilares de conteúdo da Proesc (research-brief.md)
output:
  - raw_sources: Lista de 5-8 fontes encontradas com URL, título, data, resumo e relevância
---

# Find News & Sources

Busca as notícias, estudos e dados mais relevantes sobre o tema definido pelo usuário para alimentar a criação de conteúdo da Proesc.

## Process

1. **Ler o foco de pesquisa** em `squads/proesc-social/output/research-focus.md` — extrair o tema e o recorte temporal.

2. **Executar buscas web** com pelo menos 3 queries distintas:
   - `"{tema}" gestão escolar Brasil {recorte temporal}`
   - `"{tema}" escola educação dados pesquisa {recorte temporal}`
   - `"{tema}" site:inep.gov.br OR site:mec.gov.br OR site:todospelaeducacao.org.br`

3. **Filtrar por relevância para gestores escolares**: A notícia/dado tem implicação direta no dia a dia de um diretor ou administrador escolar brasileiro? Se não, descarta.

4. **Verificar data e fonte**: Apenas fontes dentro do recorte temporal solicitado. Fontes primárias (governo, institutos, veículos jornalísticos) têm prioridade.

5. **Coletar para cada fonte**: título, URL, data de publicação, veículo/instituto, e frase resumo de por que é relevante para gestores da Proesc.

## Output Format

```yaml
research_focus:
  topic: "..."
  time_range: "..."

sources:
  - rank: 1
    title: "..."
    url: "..."
    date: "YYYY-MM-DD"
    outlet: "..."
    relevance_summary: "Por que isso importa para gestores escolares: ..."
    data_highlight: "Dado ou fato mais impactante: ..."
    pillar: "educacional | prova_social | produto | cultura | engajamento"
```

## Output Example

> Use como referência de qualidade.

```yaml
research_focus:
  topic: "inadimplência escolar 2025"
  time_range: "Últimos 30 dias"

sources:
  - rank: 1
    title: "Inadimplência escolar bate recorde no 1º trimestre de 2025"
    url: "https://www.estadao.com.br/educacao/inadimplencia-escolar-recorde-2025"
    date: "2025-03-12"
    outlet: "Estadão"
    relevance_summary: "Dado nacional recente que valida dor central dos gestores — cobrança e inadimplência"
    data_highlight: "18,3% de inadimplência média nacional no 1T25, alta de 2,1pp vs 1T24"
    pillar: "educacional"
  - rank: 2
    title: "Pesquisa ABESC 2025: gestão financeira é o maior desafio das escolas privadas"
    url: "https://abesc.org.br/pesquisa-2025-gestao-financeira"
    date: "2025-02-28"
    outlet: "ABESC"
    relevance_summary: "Pesquisa de associação setorial com 1.200 escolas — alta credibilidade para Proesc usar como fonte"
    data_highlight: "73% das escolas privadas indicam gestão financeira como principal desafio operacional"
    pillar: "educacional"
```

## Quality Criteria

- [ ] Mínimo de 5 fontes encontradas
- [ ] Todas as fontes têm URL verificável e data dentro do recorte temporal
- [ ] Pelo menos 2 fontes têm dado quantitativo (percentual, número, comparativo)
- [ ] Todas as fontes têm relevância explicada em 1 frase clara

## Veto Conditions

Reject and redo if ANY are true:
1. Menos de 5 fontes encontradas — pesquisa insuficiente
2. Alguma fonte está fora do recorte temporal solicitado sem justificativa explícita
