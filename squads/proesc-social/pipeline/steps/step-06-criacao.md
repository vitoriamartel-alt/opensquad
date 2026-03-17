---
execution: subagent
agent: squads/proesc-social/agents/caio-copy
inputFile: squads/proesc-social/output/selected-angle.md
outputFile: squads/proesc-social/output/content-draft.md
model_tier: powerful
---

# Step 06: Criação de Conteúdo Multi-Plataforma

## Context Loading

Load these files before executing:
- `squads/proesc-social/output/selected-angle.md` — Ângulo escolhido com hook e estrutura narrativa
- `squads/proesc-social/output/selected-story.md` — Pauta com dado central e fonte
- `squads/proesc-social/pipeline/data/tone-of-voice.md` — 6 tons disponíveis — **apresentar ao usuário e aguardar escolha antes de escrever**
- `squads/proesc-social/pipeline/data/output-examples.md` — Exemplos completos de qualidade
- `squads/proesc-social/pipeline/data/anti-patterns.md` — Anti-padrões a evitar
- `squads/proesc-social/_memory/memories.md` — Histórico de tons usados anteriormente

## Instructions

### Process

**IMPORTANTE: Antes de escrever qualquer conteúdo, apresentar os 6 tons e aguardar a escolha do usuário.**

1. Ler tone-of-voice.md e apresentar as 6 opções ao usuário:
   ```
   Qual tom usar para esse conteúdo?
   1. Educativo-Autoridade — dados e análise, ideal para LinkedIn
   2. Provocador-Estratégico — urgência e desafio, ideal para Instagram/TikTok
   3. Parceiro-Empático — acolhimento e comunidade, ideal para Stories/Facebook
   4. Inspirador-Transformador — visão de futuro, ideal para Reels/TikTok
   5. Técnico-Confiável — demonstrações e tutoriais, ideal para YouTube
   6. Social Proof-Baseado — depoimentos e casos reais, ideal para qualquer plataforma
   ```
   Aguardar seleção. Registrar em selected-angle.md como `tone_selected`.

2. Com o tom confirmado, executar as tarefas em sequência:
   - `create-instagram.md` — Carrossel Feed
   - `create-linkedin.md` — Post de texto
   - `create-youtube.md` — Roteiro
   - `create-facebook.md` — Post
   - `create-tiktok.md` — Script de vídeo
   - `optimize-content.md` — Revisão e otimização final

3. Salvar todo o conteúdo de todas as plataformas em content-draft.md.

## Output Format

```markdown
# Content Draft — [Pauta] | [Data]

**Tom selecionado:** [Nome do tom]
**Ângulo:** [Ângulo + emoção]
**Pauta:** [Título]

---

## 📱 Instagram Feed
[Conteúdo completo conforme formato de create-instagram.md]

---

## 💼 LinkedIn
[Conteúdo completo conforme formato de create-linkedin.md]

---

## 🎬 YouTube
[Roteiro completo conforme formato de create-youtube.md]

---

## 👥 Facebook
[Conteúdo completo conforme formato de create-facebook.md]

---

## 🎵 TikTok
[Script completo conforme formato de create-tiktok.md]

---

## Optimization Report
[Relatório de otimização de optimize-content.md]
```

## Output Example

Exemplo completo disponível em: `squads/proesc-social/pipeline/data/output-examples.md`

## Veto Conditions

Reject and redo if ANY are true:
1. Alguma plataforma ausente no output (todas as 5 são obrigatórias)
2. Tom não declarado no início do output

## Quality Criteria

- [ ] Tom declarado e consistente em todas as plataformas
- [ ] 5 plataformas com conteúdo completo e nativo (não adaptação)
- [ ] Optimization report incluído no final
- [ ] Todos os CTAs específicos e acionáveis
