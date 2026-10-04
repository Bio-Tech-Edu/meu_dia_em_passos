# GEMINI.md: instruções para o Gemini CLI e o Google Antigravity

Siga integralmente as regras de @AGENTS.md. Resumo do que é essencial:

## Contexto

O "Meu Dia em Passos" é um planner visual para uma criança autista de cerca de 3 anos, não leitora, com mediação de um adulto. A especificação está em `docs/projeto-meu-dia-em-passos-v3.md`.

## Regras

1. Escreva em português do Brasil.
2. Use HTML, CSS e JS puros, sem dependências e sem chamadas de rede.
3. Nunca use dados reais de criança; use "Criança A". Não leia `/data/`.
4. Use os tokens de cor e fonte de `AGENTS.md`. Fundo liso e no máximo 5 elementos nas páginas da criança.
5. Garanta acessibilidade (WCAG AA, teclado, `alt`, `prefers-reduced-motion`) e impressão A4.
6. Nada de peças de quebra-cabeça e nada de conteúdo clínico ou prescritivo.

## Estilo de interação

Mostre um plano curto antes de agir, execute uma tarefa por vez e termine com um resumo em até 5 linhas e a próxima tarefa sugerida.
