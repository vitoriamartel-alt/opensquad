---
task: "Create Facebook Post"
order: 4
input:
  - selected_angle: Ângulo escolhido (selected-angle.md)
  - tone_of_voice: Tom selecionado
output:
  - facebook_content: Post completo para Facebook com imagem sugerida e CTA
---

# Create Facebook Post

Cria um post para o Facebook da Proesc — focado no público de gestores e pais, tom comunitário, com pergunta de engajamento e imagem sugerida.

## Process

1. **Adaptar o ângulo para Facebook**: Facebook favorece conteúdo comunitário, histórias humanizadas e posts que geram debate. Mesmo ângulo, tom mais próximo e menos técnico.

2. **Escrever a abertura**: Diferente do LinkedIn (dado) e Instagram (hook visual), no Facebook começa com humanização ou pergunta de comunidade.

3. **Desenvolver o conteúdo**: Parágrafos mais longos são aceitáveis. Inclui a pauta/dado mas com contexto de impacto na comunidade escolar.

4. **Sugerir imagem**: Foto de escola real, evento escolar, ou infográfico — nada de stock genérico.

5. **Fechar com pergunta de comunidade**: Não um CTA de produto — uma pergunta que gera debate entre gestores.

## Output Format

```
=== FACEBOOK ===

=== IMAGEM SUGERIDA ===
[Direção de imagem — tipo, composição, texto sobreposto se necessário]

=== TEXTO ===
[Abertura — 1-3 frases humanizadas ou pergunta de comunidade]

[Desenvolvimento — contexto da pauta com impacto humano]

[Dado central incluído naturalmente no texto]

[Pergunta de comunidade ou CTA soft]

=== CTA OPCIONAL ===
[Link nos comentários ou menção ao recurso Proesc — sem ser intrusivo]
```

## Output Example

```
=== FACEBOOK ===

=== IMAGEM SUGERIDA ===
Foto de diretora conversando com professores no corredor da escola — ambiente natural, não posado. Overlay com texto: "14h por mês em cobranças. Isso pode mudar."

=== TEXTO ===
Quase todo diretor de escola que conheço entrou na educação por amor ao pedagógico.

E acabou dedicando boa parte do seu tempo a planilhas de inadimplência, cobranças manuais e follow-up de responsáveis.

O último levantamento nacional mostra que a inadimplência escolar chegou a 18,3% no início de 2025 — o maior índice desde 2019. Em números práticos: se sua escola tem 300 alunos pagando R$800/mês, são quase R$44.000 que não chegam todo mês.

Mas o dado que mais nos chamou a atenção foi outro: gestores gastam em média 14 horas por mês em cobranças que poderiam ser automatizadas.

São 14 horas que poderiam estar em reunião pedagógica. Com professores. Com alunos. Com pais que precisam de atenção — não de ligação de cobrança.

Essa é uma conversa que a gente precisa ter com mais frequência no setor.

Como vocês estão lidando com esse desafio na escola de vocês? O processo de cobrança ainda é manual, ou já automatizaram alguma coisa?

=== CTA OPCIONAL ===
[Para quem quiser conhecer como funciona a automação de cobrança da Proesc, o link está nos comentários — é gratuito para explorar]
```

## Quality Criteria

- [ ] Tom comunitário e humanizado (diferente do LinkedIn e Instagram)
- [ ] Dado da pauta incluído naturalmente no texto
- [ ] Termina com pergunta genuína que gera debate
- [ ] Imagem sugerida com direção específica (não "coloque uma foto")
- [ ] CTA de produto é suave e opcional — não é o foco do post

## Veto Conditions

Reject and redo if ANY are true:
1. Post é cópia do caption do Instagram — deve ser reescrito para Facebook
2. CTA de produto é agressivo ou domina o post
