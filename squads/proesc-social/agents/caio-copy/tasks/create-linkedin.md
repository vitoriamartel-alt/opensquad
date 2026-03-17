---
task: "Create LinkedIn Post"
order: 2
input:
  - selected_angle: Ângulo escolhido (selected-angle.md)
  - instagram_content: Conteúdo do Instagram já criado (para manter consistência de pauta, não copiar)
  - tone_of_voice: Tom selecionado
output:
  - linkedin_content: Post completo com hook, corpo, insights, CTA e hashtags
---

# Create LinkedIn Post

Cria um post de LinkedIn completo para a Proesc — nativo à plataforma, escrito em primeira pessoa, com estrutura de dwell time alto e CTA de comentário.

## Process

1. **Adaptar o ângulo para LinkedIn**: LinkedIn favorece tom educacional/autoridade e primeira pessoa. Mesmo ângulo, voz diferente — não é cópia do Instagram.

2. **Escrever o hook** (primeiros 210 chars): deve ser uma afirmação surpreendente, dado provocador, ou pergunta que cria dissonância cognitiva. Sem saudação, sem introdução genérica.

3. **Construir o corpo** em parágrafos de 1-2 frases com quebras de linha. Usar "eu" e primeira pessoa. Contar o contexto da pauta como insight pessoal ou observação de mercado.

4. **Listar 5 insights** acionáveis numerados — estes são o coração do post e o que gera salvamentos.

5. **Escrever o fechamento** com 1-2 frases de takeaway + pergunta genuína para comentários.

6. **Adicionar hashtags** (3-5) na última linha, separados do corpo.

7. **NUNCA colocar link no corpo** — post é conteúdo puro. Link vai nos comentários se necessário.

## Output Format

```
=== LINKEDIN ===

=== HOOK ===
[Primeiros ~210 caracteres — afirmação ou dado que compele "ver mais"]

=== CORPO ===
[Parágrafo de contexto — 1-2 frases, primeira pessoa]

[Parágrafo de observação — 1-2 frases]

[Transição para insights]

=== INSIGHTS ===
1. [Insight acionável — 1 frase]
2. [Insight acionável — 1 frase]
3. [Insight acionável — 1 frase]
4. [Insight acionável — 1 frase]
5. [Insight acionável — 1 frase]

=== FECHAMENTO ===
[Takeaway de 1-2 frases]

[Pergunta genuína para comentários]

=== HASHTAGS ===
#hashtag1 #hashtag2 #hashtag3
```

## Output Example

```
=== LINKEDIN ===

=== HOOK ===
87% dos diretores de escola dizem que a maior fonte de estresse não é pedagógica. É administrativa.

=== CORPO ===
Pesquisei isso com 500 gestores escolares brasileiros nos últimos 6 meses.

O resultado me surpreendeu — e provavelmente vai surpreender você.

A maioria dos diretores que conheço entrou na educação por amor à aprendizagem.
Acabaram se tornando gestores de planilha.

Matrículas. Cobranças. Comunicados. Faltas. Relatórios.

Cada processo manual é um buraco de tempo — e tempo de diretor deveria estar no pedagógico.

O que diferencia as escolas mais produtivas que analisamos:

=== INSIGHTS ===
1. Automatizaram ao menos 3 processos administrativos recorrentes (matrícula, cobrança, comunicado)
2. Usam comunicação centralizada — um canal, não 5 aplicativos simultâneos
3. Têm dados em tempo real — não esperam o fim do mês para saber a inadimplência atual
4. O diretor gasta menos de 2h/semana em tarefas que um sistema faz automaticamente
5. Tomam decisões financeiras baseadas em relatório, não em feeling

=== FECHAMENTO ===
Tecnologia não resolve problemas pedagógicos. Mas libera o gestor para resolvê-los.

Qual processo administrativo mais consome o seu tempo hoje? Me conta nos comentários.

=== HASHTAGS ===
#gestaoescolar #educacao #diretordeescola #tecnologiaeducacional #liderancaeducacional
```

## Quality Criteria

- [ ] Hook dentro de 210 caracteres, sem saudação, com dado ou afirmação forte
- [ ] Post escrito em primeira pessoa com voz autêntica
- [ ] Parágrafos de 1-2 frases com quebras de linha
- [ ] 5 insights numerados no corpo
- [ ] Nenhum link externo no corpo do post
- [ ] 3-5 hashtags na última linha
- [ ] Termina com pergunta genuína (não retórica)

## Veto Conditions

Reject and redo if ANY are true:
1. Link externo no corpo do post (não nos comentários)
2. Post começa com saudação ou "Olá", "Ei," etc.
