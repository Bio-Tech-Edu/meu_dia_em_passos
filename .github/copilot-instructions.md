# Instruções do repositório para o GitHub Copilot

Projeto "Meu Dia em Passos": planner visual para uma criança autista de cerca de 3 anos, não leitora, sempre com mediação de um adulto. A especificação completa está em `docs/projeto-meu-dia-em-passos-v3.md` e as regras gerais de agente em `AGENTS.md`.

## Sempre

- Responda e escreva comentários, textos de interface e commits em **português do Brasil**.
- Use HTML, CSS e JavaScript puros, sem frameworks, sem npm e sem CDN.
- Use os tokens de cor e fonte definidos em `AGENTS.md`, sem inventar cores novas.
- Siga os ids de página `p00` a `p16`, com `p09a` e `p09b`.
- Garanta acessibilidade: `alt`, `aria-label`, teclado, foco visível, contraste AA e `prefers-reduced-motion`.
- Garanta a impressão A4 com `@page size A4` e uma `<section>` por página.

## Nunca

- Usar dados reais de criança (nome, foto, diagnóstico, terapias, alimentação). Use "Criança A" ou "[NOME]".
- Ler, criar ou sugerir arquivos em `/data/`.
- Fazer chamadas de rede, incluir analytics ou carregar fontes remotas.
- Usar peças de quebra-cabeça em ícones ou textos.
- Gerar conteúdo de diagnóstico ou prescrição, ou textos com tom de cobrança.

## Revisão de código (Copilot code review)

Ao revisar um pull request, verifique primeiro, nesta ordem:

1. Vazamento de dados pessoais.
2. Chamadas de rede.
3. Acessibilidade.
4. Regras das páginas da criança (no máximo 5 elementos, fontes mínimas, fundo liso).
5. Impressão A4.

## Mensagens de commit

`feat(p05): ...` · `fix(p07): ...` · `docs(sprint): ...` · `chore(s0): ...`
