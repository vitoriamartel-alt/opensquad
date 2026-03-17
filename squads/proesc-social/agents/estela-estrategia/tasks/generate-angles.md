---
task: "Generate 5 Angles"
order: 1
input:
  - selected_story: Pauta escolhida pelo usuário com URL, dado central e ângulos preview
  - domain_framework: Content pillars e hook types (domain-framework.md)
output:
  - angles: 5 ângulos distintos com hook, estrutura narrativa e plataforma ideal
---

# Generate 5 Angles

Transforma uma única pauta em 5 ângulos emocionalmente distintos, cada um com hook, estrutura narrativa e plataforma ideal definidos.

## Process

1. **Ler a pauta selecionada** em `squads/proesc-social/output/selected-story.md` — extrair o dado central e o contexto.

2. **Identificar as 5 lentes emocionais** obrigatórias:
   - 🔴 **Medo**: O que o gestor arrisca ao NÃO agir com base nessa informação?
   - 🟢 **Oportunidade**: Qual é a janela de vantagem aberta por esse dado antes que todos saibam?
   - 📚 **Educacional**: Como esse dado funciona? O que ele revela sobre o setor que poucos entendem?
   - ↔️ **Contrário**: Qual é a crença popular que esse dado contradiz ou desafia?
   - ⭐ **Inspiracional**: Qual é a visão de futuro possível que esse dado torna crível?

3. **Para cada ângulo, gerar**:
   - Hook (primeira linha — máx. 2 frases, scroll-stopping)
   - Estrutura narrativa em 3 partes (Abertura → Desenvolvimento → Fechamento/CTA)
   - Plataforma ideal (onde esse ângulo emocional performa melhor)
   - Formato sugerido (carrossel, post texto, roteiro, script)

4. **Verificar diversidade**: Os 5 ângulos são genuinamente distintos? Se dois são variações do mesmo medo ou oportunidade, reescrever.

5. **Recomendar 1 ângulo** com justificativa baseada na pauta + plataformas alvo da Proesc.

## Output Format

```yaml
pauta: "Título da pauta"
source_url: "..."
core_data: "Dado central que alimenta os ângulos"

angles:
  - id: "medo"
    emotion: "🔴 Medo"
    hook: "Primeira linha — máx. 2 frases"
    narrative:
      abertura: "Como o ângulo abre — 1 frase descrevendo a tensão inicial"
      desenvolvimento: "O que o conteúdo revela ou explica — 1 frase"
      fechamento: "Como fecha + CTA — 1 frase"
    platform_ideal: "Instagram | LinkedIn | TikTok | Facebook | YouTube"
    format_suggested: "carrossel | post_texto | roteiro | script_video"

  - id: "oportunidade"
    emotion: "🟢 Oportunidade"
    hook: "..."
    narrative:
      abertura: "..."
      desenvolvimento: "..."
      fechamento: "..."
    platform_ideal: "..."
    format_suggested: "..."

  # ... (repetir para educacional, contrario, inspiracional)

recommendation:
  angle_id: "medo"
  reason: "Justificativa de 2-3 frases para a plataforma + pauta específica"
```

## Output Example

```yaml
pauta: "Inadimplência escolar bate 18,3% no 1T25"
source_url: "https://estadao.com.br/inadimplencia-escolar-2025"
core_data: "18,3% de inadimplência em escolas privadas no 1T25 — maior índice desde 2019"

angles:
  - id: "medo"
    emotion: "🔴 Medo"
    hook: "Sua escola vai receber só 81% do que é devido esse trimestre. E o problema piora se você não agir agora."
    narrative:
      abertura: "Apresenta o dado + quantifica a perda financeira concreta para uma escola de 200 alunos"
      desenvolvimento: "Mostra como cobrança manual amplifica o problema: timing errado, mensagens ignoradas, sem automação"
      fechamento: "Escolas que automatizaram cobranças reduziram inadimplência em 60% em 90 dias — CTA: solicite demo"
    platform_ideal: "Instagram"
    format_suggested: "carrossel"

  - id: "oportunidade"
    emotion: "🟢 Oportunidade"
    hook: "Enquanto 18% das escolas não recebem o que é devido, algumas operam com menos de 5% de inadimplência. A diferença é um único processo."
    narrative:
      abertura: "Apresenta a disparidade entre escolas de alta e baixa inadimplência como dado de abertura"
      desenvolvimento: "Revela que o fator diferenciador é automação de cobrança — não 'cobrar mais agressivo'"
      fechamento: "Apresenta a Proesc como o processo específico que separa os dois grupos — CTA soft: saiba mais"
    platform_ideal: "LinkedIn"
    format_suggested: "post_texto"

  - id: "educacional"
    emotion: "📚 Educacional"
    hook: "18,3% de inadimplência parece um número. Mas para uma escola de 300 alunos, significa R$43.920 que não entram por mês."
    narrative:
      abertura: "Contextualiza o dado: transforma percentual abstrato em R$ concreto para diferentes portes de escola"
      desenvolvimento: "Explica os 3 fatores que mais contribuem para inadimplência escolar: timing, canal e fricção no pagamento"
      fechamento: "Oferece checklist de diagnóstico gratuito — CTA educacional sem pressão de venda"
    platform_ideal: "LinkedIn"
    format_suggested: "carrossel_documento"

  - id: "contrario"
    emotion: "↔️ Contrário"
    hook: "A maioria das escolas trata inadimplência como problema do responsável. Na verdade, é um problema de processo interno."
    narrative:
      abertura: "Confronta a crença de que inadimplência é culpa dos pais irresponsáveis"
      desenvolvimento: "Apresenta dado: escolas com mesmo perfil socioeconômico têm taxas de inadimplência muito diferentes — a variável é o processo"
      fechamento: "Convida o gestor a reavaliar seu processo antes de culpar o cliente — link para conteúdo técnico"
    platform_ideal: "Instagram"
    format_suggested: "carrossel"

  - id: "inspiracional"
    emotion: "⭐ Inspiracional"
    hook: "Uma escola no Pará tinha 21% de inadimplência. Em 4 meses, baixou para 6%. Sem contratar ninguém. Sem ligar para nenhum responsável."
    narrative:
      abertura: "Conta a história da escola — o contexto de ponto de partida, o problema e a decisão"
      desenvolvimento: "Mostra a transformação: o antes, o processo que mudou, o depois em números reais"
      fechamento: "Inspira o gestor a imaginar o mesmo resultado para sua escola — CTA: fale com especialista"
    platform_ideal: "TikTok"
    format_suggested: "script_video"

recommendation:
  angle_id: "medo"
  reason: "Para a pauta de inadimplência, o ângulo medo tem o maior potencial no Instagram porque cria urgência imediata — gestores identificam a dor antes do scroll. O hook quantifica a perda concreta, o que no contexto de início de trimestre (março) cria alta relevância. Recomendado para carrossel de 8 slides no Instagram Feed."
```

## Quality Criteria

- [ ] Exatamente 5 ângulos gerados, um por emoção obrigatória
- [ ] Cada ângulo tem hook (máx. 2 frases), narrativa em 3 partes, plataforma e formato
- [ ] Os 5 ângulos são genuinamente distintos — nenhum é variação de outro
- [ ] Todos os 5 ângulos se referem à mesma pauta (mesmo dado central)
- [ ] Uma recomendação explícita com ângulo e justificativa de 2-3 frases

## Veto Conditions

Reject and redo if ANY are true:
1. Algum ângulo muda a pauta original (fala de outro assunto que não o dado central)
2. Dois ou mais ângulos têm o mesmo hook emocional (variações do mesmo medo, etc.)
