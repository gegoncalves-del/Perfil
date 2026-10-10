# Perfil — Analista de Marketing com Claude Code

Configuração que transforma o Claude Code em um **analista de marketing digital**.
Você informa seus dados (nome, objetivo, foco, público…) e o perfil a ser avaliado;
o analista gera diagnóstico, métricas, SWOT e um plano de ação priorizado.

## Estrutura

```
CLAUDE.md                          # Papel, método e regras do analista (carregado automaticamente)
.claude/agents/analista-marketing.md   # Subagente especialista
.claude/skills/briefing/           # Comando /briefing (entrevista guiada)
.claude/skills/analisar-perfil/    # Comando /analisar-perfil <perfil>
briefing/BRIEFING.md               # SEUS dados: objetivo, foco, público, metas
perfis/<nome>/perfil.md            # Dados do perfil avaliado (+ prints/CSVs)
templates/                         # Modelos de perfil e de relatório
relatorios/                        # Relatórios gerados
```

## Como usar

1. Abra o projeto no Claude Code (`claude` na pasta do repositório).
2. Preencha o briefing:
   - edite `briefing/BRIEFING.md`, **ou**
   - digite `/briefing` e responda às perguntas (pode colar um texto livre com tudo).
3. Crie a pasta do perfil:
   ```bash
   mkdir -p perfis/meu-perfil
   cp templates/perfil-template.md perfis/meu-perfil/perfil.md
   ```
   Preencha os dados e, se quiser, adicione prints e planilhas na mesma pasta.
4. Rode a análise:
   ```
   /analisar-perfil meu-perfil
   ```
5. O relatório fica em `relatorios/AAAA-MM-DD_meu-perfil.md`.

Também dá para conversar livremente — o `CLAUDE.md` mantém o Claude no papel de analista.
Exemplos:
- "Reescreva a bio do meu-perfil alinhada ao objetivo do briefing."
- "Monte um calendário editorial de 30 dias para o meu-perfil."
- "Use o analista-marketing para comparar meu-perfil com os concorrentes do briefing."

## Personalizar
- Mudou o método ou o formato? Edite `CLAUDE.md` e `templates/relatorio-template.md`.
- Quer outro especialista (ex.: copywriter, gestor de tráfego)? Duplique
  `.claude/agents/analista-marketing.md` com outro nome e ajuste as instruções.
