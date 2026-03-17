---
task: "Create Instagram Feed Content"
order: 1
input:
  - selected_angle: Ângulo escolhido com hook, estrutura narrativa e dados da pauta
  - tone_of_voice: Tom selecionado pelo usuário (tone-of-voice.md)
  - output_examples: Exemplos de qualidade (output-examples.md)
output:
  - instagram_content: Carrossel completo (8-10 slides) + caption + hashtags
---

# Create Instagram Feed Content

Cria um carrossel completo para o Instagram Feed da Proesc baseado no ângulo selecionado, seguindo as melhores práticas de engajamento e brand voice.

## Process

1. **Ler o ângulo selecionado** em `squads/proesc-social/output/selected-angle.md` — extrair hook, estrutura narrativa e dado central.

2. **Ler o tom selecionado** em `squads/proesc-social/pipeline/data/tone-of-voice.md` — aplicar o tom em cada linha escrita.

3. **Escolher o formato de carrossel** mais adequado ao ângulo:
   - Medo → Problema → Solução
   - Oportunidade → Antes e Depois
   - Educacional → Listicle ou Tutorial
   - Contrário → Mito vs Realidade
   - Inspiracional → Storytelling

4. **Escrever cada slide** com hierarquia de dois níveis:
   - Headline (bold, grande): ponto principal do slide — máx. 15 palavras
   - Supporting text: contexto, dado ou elaboração — 40-80 palavras

5. **Escrever a caption** com hook nos primeiros 125 chars, corpo, pergunta/CTA final.

6. **Selecionar hashtags** (5-15): 3-5 niche + 3-5 mid-range + 2-3 broad + 1-2 brand.

## Output Format

```
=== TOM SELECIONADO ===
[Nome do tom e justificativa de 1 frase]

=== FORMATO ===
[Nome do formato: Problema→Solução | Listicle | Tutorial | Mito vs Realidade | Antes e Depois | Storytelling]

=== SLIDES ===
Slide 1 (Cover):
  Title: [Título bold — máx. 20 palavras]
  Photo: [Direção fotográfica / tipo de imagem]
  Background: [escuro / claro / acento]

Slide 2 ([Papel narrativo]):
  Headline: [Ponto principal — máx. 15 palavras]
  Supporting text: [40-80 palavras de contexto ou dado]
  Accent keywords: [Palavras a destacar em cor de acento]
  Photo: [Direção fotográfica, se aplicável]
  Background: [escuro / claro / acento]

[...repetir para todos os slides...]

Slide N (CTA):
  Photo: [Interface Proesc ou imagem de conclusão]
  Source: [Fonte do dado principal]
  CTA: [Ação específica — ex: "Comenta MATRÍCULA que eu te mando o guia"]

=== CAPTION ===
[Hook — primeiros 125 chars que funcionam como standalone]

[Corpo — argumento em parágrafos curtos com quebras de linha]

[Pergunta de engajamento]

=== HASHTAGS ===
#hashtag1 #hashtag2 #hashtag3 [5-15 total]
```

## Output Example

> Adapte o conteúdo, não o formato.

```
=== TOM SELECIONADO ===
Provocador-Estratégico — A pauta de inadimplência pede urgência e dado de impacto imediato.

=== FORMATO ===
Problema → Solução (8 slides)

=== SLIDES ===
Slide 1 (Cover):
  Title: Sua escola está perdendo R$4.200/mês sem perceber
  Photo: Diretora com expressão preocupada olhando para tela de computador
  Background: Escuro com texto laranja

Slide 2 (Problema — Dado):
  Headline: 18,3% de inadimplência escolar no Brasil em 2025
  Supporting text: Em uma escola com 300 alunos pagando R$800/mês, isso são R$43.920 que não entram por mês. E a tendência é de alta — maior índice desde 2019. Se você está na média, o problema já chegou na sua escola.
  Accent keywords: R$43.920, 2019
  Background: Claro

Slide 3 (Agravante):
  Headline: Cobrança manual transforma um problema em crise
  Supporting text: Cada semana de atraso na abordagem reduz a chance de receber em 23%. Planilha não lembra. E-mail se perde. Ligação interrompe o responsável no trabalho. O processo errado agrava o problema certo.
  Accent keywords: 23%
  Background: Escuro

Slide 4 (Consequência):
  Headline: O diretor perde 14h/mês em cobranças que deveriam ser automáticas
  Supporting text: São quase 2 dias de trabalho por mês gastos em tarefas administrativas que um sistema resolve em 30 minutos de configuração. Tempo que poderia ir para o pedagógico, para o time, para os alunos.
  Accent keywords: 14h/mês, 30 minutos
  Background: Acento laranja

Slide 5 (Virada):
  Headline: A solução não é cobrar mais — é cobrar melhor
  Supporting text: Escolas que automatizaram o processo de cobrança reduziram inadimplência em 60% nos primeiros 3 meses. O segredo: cobrar no momento certo, no canal certo, sem deixar passar o timing.
  Accent keywords: 60%
  Background: Claro

Slide 6 (Solução):
  Headline: Proesc automatiza toda a jornada de cobrança
  Supporting text: Do vencimento ao recebimento: boletos automáticos, alertas por WhatsApp e e-mail no timing ideal, relatório em tempo real de inadimplentes, negativação automática para casos críticos.
  Accent keywords: tempo real, automático
  Background: Escuro

Slide 7 (Prova):
  Headline: "Em 4 meses, baixei de 19% para 6% de inadimplência"
  Supporting text: Luciana M., diretora da Escola Novo Horizonte (Belém-PA). "Antes eu passava as manhãs de segunda ligando para responsáveis. Hoje o sistema faz isso enquanto eu estou na reunião pedagógica."
  Photo: Foto de diretora sorrindo (usar ilustração neutra se não disponível)
  Background: Claro com acento

Slide 8 (CTA):
  Photo: Interface do módulo financeiro do Proesc
  Source: Dados internos Proesc — análise de 1.500+ escolas parceiras
  CTA: Comenta INADIMPLÊNCIA abaixo 👇 que eu te mando o guia gratuito de automação de cobrança

=== CAPTION ===
Sua escola está perdendo dinheiro todo mês. E o pior: você sabe quanto — mas o processo para resolver parece complicado demais.

Não é.

Analisamos o comportamento de cobrança em 1.500+ escolas e descobrimos que 73% do problema vem de um fator: o timing da abordagem.

Arrasta o carrossel para ver como resolver em 4 passos.

↓ Qual é o maior desafio de cobrança na sua escola? Comenta abaixo 👇

=== HASHTAGS ===
#gestaoescolar #inadimplenciaescolar #diretordeescola #sistemaescolar #proesc #automatizacaoescolar #financeiroeducacional #escolaprivada #gestaoeducacional #tecnologiaeducacional
```

## Quality Criteria

- [ ] Cover slide com título bold que para o scroll (máx. 20 palavras)
- [ ] Cada slide tem dois níveis de hierarquia (headline + supporting text)
- [ ] Cada slide tem 40-80 palavras de supporting text
- [ ] Background alterna entre claro/escuro/acento ao longo do carrossel
- [ ] Caption tem 125 chars de hook funcional antes da quebra
- [ ] Caption termina com pergunta de engajamento
- [ ] Hashtags entre 5-15, mix de niche e broad

## Veto Conditions

Reject and redo if ANY are true:
1. Algum slide tem menos de 40 palavras de supporting text — conteúdo raso
2. Caption começa com saudação ("Olá!", "Oi,", "Ei,")
