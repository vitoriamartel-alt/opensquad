---
task: "Optimize Content Across Platforms"
order: 6
input:
  - all_platform_content: Todo o conteúdo criado nas tarefas 1-5
  - tone_of_voice: Tom selecionado
  - anti_patterns: Lista de anti-padrões (anti-patterns.md)
output:
  - optimized_content: Conteúdo revisado e otimizado para cada plataforma + resumo de mudanças
---

# Optimize Content Across Platforms

Revisa o conteúdo criado para todas as plataformas em uma segunda passagem de otimização — consistência de voz, hooks mais fortes, e verificação de anti-padrões antes de passar para revisão.

## Process

1. **Ler todo o conteúdo criado** nas 5 tarefas anteriores.

2. **Verificar consistência de tom**: O tom selecionado em tone-of-voice.md está consistente em todas as plataformas? A Proesc soou como a mesma marca em todos os canais, mesmo com estilos diferentes?

3. **Fortalecer hooks onde necessário**: Relê a primeira frase de cada plataforma. Pode ser mais direto? Mais surpreendente? Mais específico? Se sim, reescreve.

4. **Verificar CTAs**: Cada plataforma tem exatamente um CTA específico e acionável? "Saiba mais" é inaceitável — substituir por ação concreta.

5. **Verificar anti-padrões**: Passar pelo checklist de anti-patterns.md. Algum padrão negativo se infiltrou? (link no corpo do LinkedIn, slides sem supporting text, TikTok sem texto na tela, etc.)

6. **Verificar dados**: Os números e afirmações estão alinhados com research-brief.md? Alguma afirmação não tem fonte?

7. **Entregar versão final**: Conteúdo completo com indicação de quais mudanças foram feitas e por quê.

## Output Format

```
=== OPTIMIZATION REPORT ===

Tom aplicado: [nome do tom]
Consistência de tom: [CONSISTENTE / INCONSISTENTE — ajuste X feito]

=== INSTAGRAM (VERSÃO FINAL) ===
[Conteúdo completo — apenas se alterado. Se sem mudança: "Sem alterações."]
Mudança feita: [descrição da otimização, se houver]

=== LINKEDIN (VERSÃO FINAL) ===
[Conteúdo completo ou "Sem alterações"]
Mudança feita: [...]

=== YOUTUBE (VERSÃO FINAL) ===
[Roteiro completo ou "Sem alterações"]
Mudança feita: [...]

=== FACEBOOK (VERSÃO FINAL) ===
[Conteúdo completo ou "Sem alterações"]
Mudança feita: [...]

=== TIKTOK (VERSÃO FINAL) ===
[Script completo ou "Sem alterações"]
Mudança feita: [...]

=== ANTI-PATTERN CHECK ===
- [ ] LinkedIn sem link no corpo ✅/❌
- [ ] Instagram: hooks nos primeiros 125 chars ✅/❌
- [ ] TikTok: texto na tela em todos os blocos ✅/❌
- [ ] Todos os CTAs específicos e acionáveis ✅/❌
- [ ] Nenhum dado sem fonte em research-brief.md ✅/❌
```

## Quality Criteria

- [ ] Todos os 5 plataformas revisadas e declaradas (com ou sem mudanças)
- [ ] Anti-pattern checklist completo com status
- [ ] Mudanças documentadas com justificativa
- [ ] Tom declarado e confirmado como consistente

## Veto Conditions

Reject and redo if ANY are true:
1. Anti-pattern checklist tem item ❌ não corrigido
2. Alguma plataforma não foi revisada (apenas 3 de 5, por exemplo)
