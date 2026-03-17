---
task: "Consolidate & Package Output"
order: 1
input:
  - approved_content: Conteúdo aprovado pelo usuário no checkpoint step-07
  - domain_framework: Calendário editorial e timing de publicação (domain-framework.md)
  - squad_memory: Histórico de hashtags e pautas usadas (memories.md)
output:
  - content_package: Pacote de publicação organizado por plataforma com checklist
  - updated_memory: Atualização do squad memory com pauta e tom deste run
---

# Consolidate & Package Output

Organiza o conteúdo aprovado em um pacote de publicação profissional — estruturado por plataforma, com checklist de ações, timing sugerido e conjuntos de hashtags rotacionados.

## Process

1. **Ler o conteúdo aprovado** em `squads/proesc-social/output/content-approved.md`.

2. **Separar por plataforma**: Criar seção clara para cada uma das 5 plataformas.

3. **Gerar checklist de publicação** para cada plataforma com ações específicas e ordenadas:
   - Instagram: Design dos slides → Upload → Caption → Hashtags → Agendar
   - LinkedIn: Copiar post → Publicar → Adicionar link nos comentários
   - YouTube: Roteiro → Gravar → Editar → Upload com descrição → Thumbnail
   - Facebook: Selecionar imagem → Publicar post → Adicionar link nos comentários
   - TikTok: Gravar com roteiro → Editar → Upload → Adicionar hashtags

4. **Sugerir janela de publicação** por plataforma com base em domain-framework.md:
   - LinkedIn: 7-9h ou 12-13h, Terça-Quinta
   - Instagram: 9-11h ou 19-21h, Terça-Quinta
   - TikTok: 18-21h qualquer dia da semana
   - Facebook: 13-15h, Terça-Quinta
   - YouTube: Quinta ou Sexta, 11h ou 15h

5. **Gerar conjuntos de hashtags rotacionados**: Verificar memories.md para garantir que os hashtags deste run são diferentes dos últimos 2 runs.

6. **Sinalizar pending_visual** onde necessário: carrossel do Instagram e script do TikTok/YouTube precisam de produção visual antes de publicar.

7. **Atualizar squad memory**: Registrar pauta, ângulo, tom e data deste run.

## Output Format

```markdown
# Pacote de Publicação — [Data]

**Pauta:** [Título da pauta]
**Ângulo:** [Ângulo escolhido + emoção]
**Tom:** [Tom selecionado]
**Gerado em:** [Data]

---

## 📱 Instagram Feed

**Status:** ⚠️ PENDING VISUAL — carrossel precisa ser criado em Canva/ferramenta de design
**Conteúdo aprovado:** ✅

### Caption pronto para copiar:
[Caption completa]

### Hashtags (Conjunto A):
[#hashtags]

### Checklist de publicação:
- [ ] Criar slides do carrossel (8-10 slides)
- [ ] Fazer upload como post (não Story)
- [ ] Colar caption — verificar quebras de linha
- [ ] Adicionar hashtags no final da caption
- [ ] Agendar para: [Dia da semana], [Horário] (ou publicar agora)

---

## 💼 LinkedIn

**Status:** ✅ PRONTO PARA PUBLICAR
**Conteúdo aprovado:** ✅

### Post pronto para copiar:
[Post completo]

### Checklist de publicação:
- [ ] Copiar post
- [ ] Publicar sem adicionar link no corpo
- [ ] Adicionar link [URL da Proesc] nos primeiros comentários
- [ ] Agendar para: [Dia da semana], [Horário]

---

## 🎬 YouTube

**Status:** ⚠️ PENDING PRODUÇÃO — roteiro pronto, vídeo precisa ser gravado
**Conteúdo aprovado:** ✅

### Roteiro aprovado: [ver content-approved.md — seção YouTube]

### Checklist de publicação:
- [ ] Gravar vídeo seguindo roteiro
- [ ] Editar com B-rolls sugeridos
- [ ] Criar thumbnail: [descrição da thumbnail]
- [ ] Upload com título: [sugestão de título SEO]
- [ ] Descrição: [primeiras linhas da descrição sugerida]
- [ ] Publicar: [Dia da semana], [Horário]

---

## 👥 Facebook

**Status:** ⚠️ PENDING IMAGEM — selecionar ou criar imagem antes de publicar
**Conteúdo aprovado:** ✅

### Post pronto para copiar:
[Post completo]

### Checklist de publicação:
- [ ] Selecionar imagem (direção: [descrição])
- [ ] Publicar post com imagem
- [ ] Adicionar link nos comentários se aplicável
- [ ] Agendar para: [Dia da semana], [Horário]

---

## 🎵 TikTok

**Status:** ⚠️ PENDING GRAVAÇÃO — script pronto, vídeo precisa ser gravado
**Conteúdo aprovado:** ✅

### Script aprovado: [ver content-approved.md — seção TikTok]

### Hashtags TikTok:
[#hashtags]

### Checklist de publicação:
- [ ] Gravar vídeo de acordo com o script (formato vertical 9:16)
- [ ] Adicionar texto na tela conforme indicado no script
- [ ] Adicionar som/trilha sugerido
- [ ] Upload no TikTok
- [ ] Adicionar hashtags
- [ ] Publicar: [Horário entre 18-21h]

---

## 📋 Squad Memory Update

Registrado automaticamente:
- **Pauta usada:** [título]
- **Ângulo:** [ângulo]
- **Tom:** [tom]
- **Data:** [YYYY-MM-DD]
- **Hashtags utilizados (Instagram):** [lista para evitar repetição]
```

## Quality Criteria

- [ ] Todas as 5 plataformas têm seção com status (PRONTO / PENDING VISUAL / PENDING PRODUÇÃO)
- [ ] Cada plataforma tem checklist de publicação com ações específicas
- [ ] Timing de publicação sugerido com dia e horário para cada plataforma
- [ ] pending_visual / pending_produção sinalizados onde aplicável
- [ ] Squad memory atualizado com pauta, ângulo, tom e data

## Veto Conditions

Reject and redo if ANY are true:
1. Alguma das 5 plataformas não tem seção no pacote
2. Squad memory não foi atualizado
