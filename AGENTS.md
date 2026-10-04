# AGENTS.md: instruções para agentes de IA

Este arquivo é lido por agentes de código como OpenAI Codex, GitHub Copilot (modo agente), Cursor, Cline e Google Antigravity, e serve de base para `CLAUDE.md` e `GEMINI.md`.

## Projeto

"Meu Dia em Passos" é um planner visual para uma criança autista de cerca de 3 anos, não leitora, sempre usado com a mediação de um adulto. Ele organiza a rotina, as transições, as emoções, a alimentação e o acompanhamento terapêutico, com baixa carga sensorial.

- Especificação: `docs/projeto-meu-dia-em-passos-v3.md`, principalmente a seção 7.
- Plano de trabalho: `docs/sprints-meu-dia-em-passos-v2.md`.
- Público dos textos: famílias e terapeutas no Brasil. **Todo texto visível deve estar em português do Brasil.**

## Regras invioláveis

1. **Privacidade (LGPD):** nunca crie, peça, registre ou envie dados reais de criança, como nome, foto, diagnóstico, terapias, alimentação ou observações clínicas. Use apenas "Criança A" ou "[NOME]". A pasta `/data/` está no `.gitignore` e não deve ser lida nem versionada.
2. **Sem rede:** a versão digital não faz nenhuma chamada de rede. Isso exclui CDN, fontes remotas, analytics, rastreadores e APIs.
3. **Sem dependências:** use somente HTML, CSS e JavaScript puros. Sem frameworks, sem npm e sem bibliotecas externas.
4. **Sem peças de quebra-cabeça** em ícones, imagens ou textos. O símbolo do projeto é o infinito colorido.
5. **Linguagem positiva e literal:** sem cobrança, culpa ou termos capacitistas. Na alimentação, nada de pressão ("oferecer não é obrigar").
6. O planner **não substitui orientação profissional**. Nunca gere conteúdo de diagnóstico ou de prescrição.

## Estrutura

```text
docs/       especificação e plano (Markdown)
prompts/    prompts por tipo de IA
src/        versão digital: index.html, styles.css, app.js, data/cartoes.json (dados fictícios)
assets/     icons/ (pictogramas licenciados), mascote/, paginas/ (PNG exportados do Canva)
```

As páginas usam os ids `p00` a `p16`, seguindo a tabela 7.1 da especificação. A página 9 tem as subpáginas `p09a` (Meus alimentos) e `p09b` (Cadeia alimentar).

## Tokens de design

```css
:root {
  --fundo: #FFF9F0;   --texto: #3A3A3A;
  --seg: #CDB4DB;     --ter: #B7E4C7;   --qua: #BDE0FE;
  --qui: #F4A7A3;     --sex: #FFE5A0;   --fds: #FFD6BA;
  --emocao-bem: #6BBF59; --emocao-meio: #F2C14E; --emocao-mal: #E76F51;
  --fonte-titulo: "Fredoka", "Baloo 2", system-ui, sans-serif;
  --fonte-texto: "Nunito", system-ui, sans-serif;
}
```

As fontes devem ser arquivos locais em `assets/` ou cair no fallback do sistema. Nunca use Google Fonts remoto.

## Regras para as páginas da criança

As páginas da criança são `p00`, `p04`, `p05`, `p06`, `p09a`, `p11`, `p12` e `p14`.

- Fundo liso `--fundo`, sem estampas.
- No máximo 5 elementos de escolha por tela.
- Títulos com 28px ou mais e rótulos com 18px ou mais. Áreas de toque com pelo menos 48×48px.
- Cores das emoções usadas **somente** para emoções.
- Animações suaves e desligadas com `prefers-reduced-motion: reduce`.

## Acessibilidade

- HTML semântico, `alt` descritivo em todas as imagens e `aria-label` em botões com ícone.
- Navegação completa por teclado e foco visível.
- Contraste mínimo WCAG AA.
- Arrastar e soltar sempre com alternativa por teclado e por toque (Pointer Events).

## Impressão

- `@media print` com `@page { size: A4; margin: 10mm; }`.
- Uma `<section>` por página, com `break-after: page`.
- Esconder a navegação e os botões na impressão.

## Persistência

- Opcional, apenas em `localStorage`, com chaves prefixadas por `mdp-`.
- Sempre ter um botão "Apagar tudo".
- Exportar e importar em JSON somente pelo navegador (download e upload local).

## Commits e branches

- Commits: `feat(pXX): ...`, `fix(pXX): ...`, `docs(...): ...`, `chore(...): ...`.
- Branches: `sprint-NN/pXX-descricao`.
- Cada mudança de página referencia a issue `[PXX]`.

## Antes de concluir uma tarefa

- [ ] Nenhuma chamada de rede (`fetch`, `XMLHttpRequest`, `<link>` ou `<script>` externos).
- [ ] Nenhum dado pessoal real.
- [ ] Textos em português do Brasil.
- [ ] Checklist de acessibilidade ok.
- [ ] Impressão A4 testada (`Ctrl+P`).
- [ ] Resumo do que mudou e de como testar.
