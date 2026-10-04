# IA de código: instruções e prompts

**Ferramentas possíveis e arquivo que cada uma lê:**

| Ferramenta | Arquivo de instruções |
|---|---|
| GitHub Copilot (chat, agente, code review) | `.github/copilot-instructions.md` + `.github/instructions/*.instructions.md` + `AGENTS.md` |
| OpenAI Codex | `AGENTS.md` |
| Claude Code | `CLAUDE.md` (importa `AGENTS.md`) |
| Gemini CLI / Google Antigravity | `GEMINI.md` (importa `AGENTS.md`) |
| Cursor | `.cursor/rules/projeto.mdc` + `AGENTS.md` |
| Cline | `AGENTS.md` |

**Função no projeto:** criar a versão digital em `src/` (HTML, CSS e JS puros), com impressão A4, cartões arrastáveis e mapa alimentar interativo; além de estrutura do repositório e notas de versão.

## Prompts deste projeto (em `docs/sprints-meu-dia-em-passos-v2.md`)

| ID | Uso |
|---|---|
| S0.1 | Estrutura do repositório e `.gitignore` |
| S6.1 | Esqueleto da versão digital e layout A4 |
| S6.2 | Rotina com arrastar e soltar (P05) |
| S6.3 | Mapa alimentar digital (P09A e P09B) |
| S6.4 | Revisão de acessibilidade e privacidade |
| S8.2 | CHANGELOG e tag `v1.0.0` |

## Prompt extra: página genérica

```text
Leia AGENTS.md. Implemente a página [PXX – NOME] em src/ seguindo docs/projeto-meu-dia-em-passos-v3.md, seção 7.2.
Use os tokens de design, respeite as regras das páginas da criança (se aplicável), garanta impressão A4 e acessibilidade.
Sem dependências e sem rede. Mostre um plano curto antes e um resumo de até 5 linhas depois.
```
