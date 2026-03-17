---
task: "Create TikTok Script"
order: 5
input:
  - selected_angle: Ângulo escolhido (selected-angle.md)
  - tone_of_voice: Tom selecionado
output:
  - tiktok_script: Script de vídeo de 30-60s com cues de câmera, som sugerido e hooks visuais
---

# Create TikTok Script

Cria um script de vídeo para TikTok da Proesc — hook nos primeiros 3 segundos, estrutura de problema/solução em até 60 segundos, nativo ao formato vertical.

## Process

1. **Hook de 3 segundos**: A primeira frase e o visual do primeiro frame decidem se o usuário fica ou scrolla. Começa com o resultado surpreendente, o problema doloroso, ou a contradição inesperada.

2. **Estrutura em 3 blocos**: Problema (15s) → Revelação (30s) → CTA (10s). Total: ~55-60 segundos.

3. **Indicações de câmera**: TikTok é vertical (9:16). Cada cena tem instrução de câmera: close no celular, B-roll de escola, texto na tela, transição rápida.

4. **Sugerir som/trilha**: Tom do vídeo + tipo de som que combina (trending, instrumental, silêncio com texto na tela).

5. **Texto na tela**: Indicar quais frases devem aparecer como texto sobreposto — crítico para quem assiste sem som (50%+ dos usuários).

6. **CTA final**: "Segue aqui" + "Comenta X" ou "Link na bio" — específico.

## Output Format

```
=== TIKTOK SCRIPT ===
Duração estimada: [30-60 segundos]
Formato: [Falando para câmera | Screen recording | Narração + B-roll | Texto na tela]
Som sugerido: [Trending sound / Instrumental / Silêncio + texto]

[0:00 - 0:03 — HOOK VISUAL + VERBAL]
Câmera: [O que aparece no primeiro frame]
Fala: "..."
Texto na tela: "..."

[0:03 - 0:20 — PROBLEMA]
Câmera: [...]
Fala: "..."
Texto na tela: "..."

[0:20 - 0:50 — REVELAÇÃO / SOLUÇÃO]
Câmera: [...]
Fala: "..."
Texto na tela: "..."

[0:50 - 1:00 — CTA]
Câmera: [...]
Fala: "..."
Texto na tela: "..."

=== HASHTAGS ===
#hashtag1 #hashtag2 #hashtag3 [5-8 total, mix niche + trending edu]
```

## Output Example

```
=== TIKTOK SCRIPT ===
Duração estimada: 55 segundos
Formato: Falando para câmera + cortes rápidos
Som sugerido: Instrumental leve de fundo (não trending — para não datar o vídeo)

[0:00 - 0:03 — HOOK VISUAL + VERBAL]
Câmera: Close no rosto da pessoa, expressão de surpresa ou urgência
Fala: "Essa escola tinha 21% de inadimplência. Em 4 meses: 6%. Sem ligar para ninguém."
Texto na tela: "21% → 6% em 4 meses" (destaque em laranja)

[0:03 - 0:18 — PROBLEMA]
Câmera: Cut rápido para planilha ou celular com lista de cobranças
Fala: "A maioria das escolas trata inadimplência com ligações e planilhas. É isso que não funciona."
"Cada semana de atraso na cobrança reduz em 23% a chance de receber. O processo manual trabalha contra você."
Texto na tela: "Cobrança manual → 23% menos chance de receber"

[0:18 - 0:48 — REVELAÇÃO]
Câmera: Screen recording do celular mostrando sistema de cobrança automatizada (interface limpa)
Fala: "O que essa escola fez foi automatizar 3 coisas:"
"Um: alertas de vencimento 7 dias antes"
"Dois: mensagens por WhatsApp no timing exato"
"Três: relatório em tempo real — sem esperar o fim do mês"
Texto na tela: "1. Alerta 7 dias antes" / "2. WhatsApp automatizado" / "3. Relatório em tempo real"
Câmera: Corte rápido entre cada ponto — ritmo dinâmico

[0:48 - 0:55 — CTA]
Câmera: Volta para câmera frontal
Fala: "Se você gerencia escola, segue aqui — toda semana tem conteúdo de gestão escolar prático. E comenta: cobrança manual ou automatizada?"
Texto na tela: "Segue para mais dicas de gestão escolar 📚"

=== HASHTAGS ===
#gestaoescolar #diretordeescola #educacao #escolaprivada #proesc #gestaofinanceira #tecnologiaeducacional
```

## Quality Criteria

- [ ] Hook visual + verbal nos primeiros 3 segundos sem saudação
- [ ] Duração estimada declarada (30-60s)
- [ ] Cada cena tem câmera + fala + texto na tela especificados
- [ ] Som/trilha sugerido
- [ ] CTA final específico (não apenas "curte e segue")
- [ ] Hashtags entre 5-8 (TikTok — menos é mais)

## Veto Conditions

Reject and redo if ANY are true:
1. Script começa com saudação nos primeiros 3 segundos
2. Nenhum texto na tela especificado — indispensável para audiência sem som
