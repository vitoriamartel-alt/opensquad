---
task: "Create YouTube Script"
order: 3
input:
  - selected_angle: Ângulo escolhido (selected-angle.md)
  - tone_of_voice: Tom selecionado
output:
  - youtube_script: Roteiro completo para vídeo de 5-10 minutos com indicações de câmera
---

# Create YouTube Script

Cria um roteiro completo para vídeo do YouTube da Proesc — estruturado para retenção, com hook nos primeiros 30 segundos, e CTAs estratégicos.

## Process

1. **Definir o formato do vídeo**: Para a pauta e ângulo, escolher entre tutorial prático (how-to), case study/história, ou análise de dado/tendência.

2. **Escrever o hook (0-30s)**: Começa com o resultado ou a provocação — nunca com "Olá, tudo bem?" O espectador decide ficar nos primeiros 30 segundos.

3. **Apresentar o problema (30-90s)**: Contextualizar a dor com dado específico. Fazer o espectador se identificar antes de apresentar solução.

4. **Desenvolver o conteúdo (90s-8min)**: Estrutura por etapas numeradas ou por revelação progressiva. Cada bloco tem cue de câmera e B-roll sugerido.

5. **Mid-video CTA (em torno da metade)**: CTA natural inserido em pausa de tópico — "Se você está gostando, salva esse vídeo."

6. **Conclusão e CTA final (último minuto)**: Resumo dos pontos + CTA específico (link na descrição, demo gratuita, próximo vídeo).

## Output Format

```
=== YOUTUBE SCRIPT ===
Formato: [Tutorial | Case Study | Análise]
Duração estimada: [X-Y minutos]
Thumbnail suggestion: [Descrição de thumbnail de alto CTR]

[0:00 - 0:30 — HOOK]
[Texto do script]
Visual cue: [O que a câmera mostra]

[0:30 - 1:30 — PROBLEMA]
[Texto do script]
Visual cue: [O que a câmera mostra / B-roll sugerido]

[1:30 - X:XX — CONTEÚDO PRINCIPAL]
Bloco 1: [Título do bloco]
[Texto do script]
Visual cue: [Screen recording / câmera / gráfico]

Bloco 2: [Título]
[...]

[MID-VIDEO CTA — aproximadamente na metade]
[Texto do script]

[X:XX - Final — CONCLUSÃO + CTA]
[Texto do script]
Visual cue: [Tela de conclusão]
End screen CTA: [Vídeo sugerido para tela final]
```

## Output Example

```
=== YOUTUBE SCRIPT ===
Formato: Tutorial Prático
Duração estimada: 7-9 minutos
Thumbnail suggestion: Split screen — planilha caótica (esquerda, tachado) vs sistema limpo (direita) + texto "De 19% para 6% em 4 meses"

[0:00 - 0:30 — HOOK]
"Essa escola aqui do Pará tinha 19% de inadimplência. Em 4 meses, chegou em 6%. Sem contratar ninguém novo. Sem ligar para nenhum pai. No vídeo de hoje, eu mostro exatamente o processo que eles usaram — e como você pode replicar na sua escola."
Visual cue: Abrir diretamente com planilha ou sistema na tela, sem introdução

[0:30 - 1:30 — PROBLEMA]
"Primeiro, deixa eu te mostrar por que a maioria das escolas trava nesse problema."
"18,3% de inadimplência média no Brasil em 2025 — maior índice desde 2019."
"Numa escola com 300 alunos pagando R$800 de mensalidade, isso são R$43.920 não recebidos todo mês. Por mês."
"E quando a cobrança é manual — planilha, WhatsApp, ligação — cada semana de atraso reduce em 23% a chance de receber. Você está num jogo que piora com o tempo."
Visual cue: Gráfico animado simples mostrando a perda acumulada

[1:30 - 3:00 — DIAGNÓSTICO]
Bloco 1: "Os 3 erros de processo que mais contribuem para inadimplência"
"Erro 1: Cobrar depois que o vencimento passou — o timing certo é ANTES."
"Erro 2: Cobrar pelo mesmo canal sempre — responsável ignora. Varie: boleto, WhatsApp, e-mail."
"Erro 3: Não segmentar a abordagem — primeiro atraso vs. recorrente precisam de mensagens diferentes."
Visual cue: Tela dividida mostrando o processo errado vs. correto

[MID-VIDEO CTA — 4:00]
"Se esse conteúdo está sendo útil pra você, salva esse vídeo — você vai querer consultar a parte dos passos de implementação depois."

[3:00 - 6:30 — SOLUÇÃO EM 4 PASSOS]
Bloco 2: "Como automatizar o processo de cobrança — passo a passo"
"Passo 1: Configure alertas automáticos 7 dias antes do vencimento [mostrar sistema]"
"Passo 2: Defina a régua de comunicação por canal — WhatsApp primeiro, e-mail como backup [mostrar fluxo]"
"Passo 3: Separe inadimplentes recentes de crônicos — abordagem diferente para cada perfil [mostrar segmentação]"
"Passo 4: Monitore em tempo real — não espere o fim do mês para saber o número [mostrar dashboard]"
Visual cue: Screen recording do sistema Proesc a cada passo — mostrar na prática

[6:30 - 7:30 — CASE STUDY]
"Deixa eu te mostrar como a Escola Novo Horizonte, em Belém, aplicou exatamente isso."
"Ponto de partida: 19% de inadimplência, cobrança 100% manual, diretor gastando 14h/mês."
"30 dias depois de implementar o processo automatizado: 11%. 90 dias: 6%."
"A diretora hoje passa as manhãs de segunda em reunião pedagógica, não ligando para responsável."
Visual cue: Depoimento da diretora ou texto do depoimento com foto

[7:30 - Final — CTA]
"Se você quer implementar esse processo na sua escola, o link está na descrição para uma demo gratuita com um especialista da Proesc."
"Eles vão analisar o processo atual da sua escola e mostrar o que muda na prática — sem compromisso."
"Até o próximo vídeo, e vejo você lá."
Visual cue: Tela de conclusão com logo + vídeo sugerido "Como reduzir faltas com comunicação automatizada"
End screen CTA: Link para demo + vídeo relacionado
```

## Quality Criteria

- [ ] Hook entregue nos primeiros 30 segundos (sem saudação inicial)
- [ ] Problema contextualizado com dado específico até 1:30
- [ ] Mid-video CTA incluído organicamente
- [ ] Cada bloco tem visual cue/sugestão de câmera ou B-roll
- [ ] CTA final específico com instrução de ação (não "check out our site")
- [ ] Duração estimada declarada

## Veto Conditions

Reject and redo if ANY are true:
1. Roteiro começa com "Olá! Bem-vindos ao canal" ou qualquer saudação similar
2. Nenhum visual cue especificado — roteiro sem direção de câmera é inutilizável
