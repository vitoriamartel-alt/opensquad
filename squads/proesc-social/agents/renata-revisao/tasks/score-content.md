---
task: "Score Content"
order: 1
input:
  - content_package: Pacote de conteúdo consolidado por plataforma (content-package.md)
  - quality_criteria: Critérios de qualidade (quality-criteria.md)
  - anti_patterns: Anti-padrões (anti-patterns.md)
  - research_brief: Dados verificáveis (research-brief.md)
output:
  - scorecard: Pontuação por critério para cada plataforma com veredito preliminar
---

# Score Content

Avalia o conteúdo de cada plataforma contra os critérios definidos em quality-criteria.md e produz um scorecard objetivo com veredito preliminar.

## Process

1. **Ler o content-package.md** completo — extrair o conteúdo de cada uma das 5 plataformas.

2. **Para cada plataforma, avaliar os critérios universais** (1-10 com justificativa):
   - Brand Voice Alignment
   - Hook Quality
   - Value Delivery
   - CTA Clarity
   - Accuracy (Pass/Fail)

3. **Para cada plataforma, avaliar os critérios específicos** da plataforma (checklist Pass/Fail).

4. **Verificar anti-padrões**: Cada item de anti-patterns.md é verificado e marcado como presente ou ausente.

5. **Calcular nota média** por plataforma (excluindo Accuracy que é Pass/Fail).

6. **Emitir veredito preliminar** por plataforma:
   - APROVADO: Todos os critérios ≥ 7/10 e Accuracy = Pass
   - APROVADO COM RESSALVAS: Algum critério entre 5-6/10, nenhum abaixo de 5, Accuracy = Pass
   - REVISÃO NECESSÁRIA: Qualquer critério < 5/10 OU Accuracy = Fail

## Output Format

```yaml
scorecard:
  run_date: "YYYY-MM-DD"
  pauta: "..."
  angulo: "..."

  platforms:
    instagram:
      universal_criteria:
        brand_voice: {score: X, justification: "..."}
        hook_quality: {score: X, justification: "..."}
        value_delivery: {score: X, justification: "..."}
        cta_clarity: {score: X, justification: "..."}
        accuracy: {pass: true/false, note: "..."}
      platform_criteria:
        cover_hook: pass/fail
        slide_hierarchy: pass/fail
        slide_word_count: pass/fail
        caption_hook_125: pass/fail
        hashtag_count: pass/fail
      average_score: X.X
      verdict: APROVADO | APROVADO COM RESSALVAS | REVISÃO NECESSÁRIA
      verdict_reason: "..."

    linkedin:
      [mesmo formato]

    youtube:
      [mesmo formato]

    facebook:
      [mesmo formato]

    tiktok:
      [mesmo formato]

  overall_verdict: APROVADO | APROVADO COM RESSALVAS | REVISÃO NECESSÁRIA
  issues_critical: [] # Bloqueadores de publicação
  issues_important: [] # Recomendações fortes
  issues_suggestion: [] # Melhorias opcionais
```

## Output Example

```yaml
scorecard:
  run_date: "2026-03-17"
  pauta: "Inadimplência escolar 18,3% no 1T25"
  angulo: "🔴 Medo — custo oculto da inadimplência manual"

  platforms:
    instagram:
      universal_criteria:
        brand_voice: {score: 9, justification: "Tom Provocador-Estratégico consistente, linguagem direta com dados concretos ao longo de todos os slides"}
        hook_quality: {score: 8, justification: "Cover slide para o scroll com dado financeiro específico — poderia ser mais urgente com data/contexto atual"}
        value_delivery: {score: 9, justification: "8 slides com dado acionável em cada um, progresso narrativo claro do problema à solução"}
        cta_clarity: {score: 8, justification: "CTA keyword 'INADIMPLÊNCIA' no último slide é específico e acionável"}
        accuracy: {pass: true, note: "Dado 18,3% confirmado em research-brief.md, fonte Estadão"}
      platform_criteria:
        cover_hook: pass
        slide_hierarchy: pass
        slide_word_count: pass
        caption_hook_125: pass
        hashtag_count: pass
      average_score: 8.5
      verdict: APROVADO
      verdict_reason: "Conteúdo sólido com brand voice forte, dados verificáveis e CTA acionável"

    linkedin:
      universal_criteria:
        brand_voice: {score: 7, justification: "Tom educacional adequado ao LinkedIn, primeira pessoa mantida"}
        hook_quality: {score: 6, justification: "Dado de 87% é forte mas poderia ser mais específico no contexto da Proesc — falta tensão imediata"}
        value_delivery: {score: 8, justification: "5 insights numerados com alto potencial de salvamento"}
        cta_clarity: {score: 9, justification: "Pergunta genuína e específica que convida resposta pessoal"}
        accuracy: {pass: true, note: "Percentual 87% declarado como pesquisa interna — verificar fonte antes de publicar"}
      platform_criteria:
        hook_210_chars: pass
        first_person: pass
        short_paragraphs: pass
        no_link_in_body: pass
        hashtag_count: pass
      average_score: 7.5
      verdict: APROVADO COM RESSALVAS
      verdict_reason: "Hook do LinkedIn pode ser mais impactante. Fonte do dado 87% deve ser declarada ou ajustada."

  overall_verdict: APROVADO COM RESSALVAS
  issues_critical: []
  issues_important:
    - "LinkedIn: Hook pode ser fortalecido — substituir dado genérico por dado da Proesc"
    - "LinkedIn: Fonte do '87%' precisa ser atribuída corretamente"
  issues_suggestion:
    - "Instagram: Cover slide pode mencionar o dado específico 18,3% para criar mais especificidade"
```

## Quality Criteria

- [ ] Todas as 5 plataformas avaliadas com scorecard completo
- [ ] Cada critério tem nota (1-10) E justificativa de 1 frase
- [ ] Veredito declarado para cada plataforma individualmente
- [ ] Veredito geral declarado
- [ ] issues_critical, issues_important, issues_suggestion preenchidos (vazios se não houver)

## Veto Conditions

Reject and redo if ANY are true:
1. Alguma plataforma sem scorecard — todas as 5 devem ser avaliadas
2. Critério com nota sem justificativa — inutilizável para gerar feedback
