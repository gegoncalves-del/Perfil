---
name: analisar-perfil
description: Executa a análise de marketing completa de um perfil (pasta em perfis/) cruzando com o briefing do projeto e gera o relatório em relatorios/.
argument-hint: <nome-do-perfil>
---

Execute uma análise de marketing completa do perfil **$ARGUMENTS**.

Passos:
1. Leia `briefing/BRIEFING.md`. Se estiver vazio ou sem objetivo definido, pare e sugira
   rodar `/briefing` primeiro.
2. Leia tudo em `perfis/$ARGUMENTS/`. Se a pasta não existir, liste as pastas disponíveis
   em `perfis/` e explique como criar uma a partir de `templates/perfil-template.md`.
3. Delegue a análise ao subagente `analista-marketing`, passando o nome do perfil.
4. Confira se o relatório foi salvo em `relatorios/` seguindo `templates/relatorio-template.md`.
5. Responda ao usuário com:
   - Nota de alinhamento com o objetivo (0–10)
   - Resumo executivo (até 5 bullets)
   - As 3 ações para os próximos 7 dias
   - Caminho do relatório completo
