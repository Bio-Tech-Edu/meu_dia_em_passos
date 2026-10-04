# Canva AI: instruções e prompts

**Função no projeto:** diagramar páginas, cartões, capa e fichas.
**Onde usar:** Canva → Canva AI → "Design for me"; no editor, use o painel do Canva AI para ajustar o design aberto.

## Configuração (uma vez só)

1. Crie o Brand Kit "Meu Dia em Passos" com a paleta e as fontes de `AGENTS.md`.
2. Crie a pasta do projeto com as subpastas Criança, Família, Equipe, Alimentação, Cartões e Final.
3. Salve o template-mestre (prompt S0.2) e sempre parta dele.

## Bloco de contexto (cole no início de cada prompt)

```text
Context: children's visual planner "Meu Dia em Passos" for a 3-year-old non-reading autistic child, used with an adult.
Brand: cream background #FFF9F0, charcoal text #3A3A3A, soft desaturated pastels, rounded title font, rainbow infinity symbol.
Rules: no patterns on child pages, max 5 choice elements, titles ≥ 28 pt, labels ≥ 18 pt, no puzzle pieces, lots of white space.
All text in Brazilian Portuguese.
```

## Prompts deste projeto (em `docs/sprints-meu-dia-em-passos-v2.md`)

| ID | Página |
|---|---|
| S0.2 | Template-mestre |
| P00, P04, P05, P06, P11, P12, P14 | Camada da criança (S2) |
| P01, P02, P03, P07, P08, P10, P13, P15 | Camadas da família e da equipe (S3) |
| P09A, P09B | Mapa de preferências alimentares (S4) |
| S5.1, S5.2, S5.3 | Cartões, cartão "tablet" e envelope "ACABOU" |
| S7.1 | Ficha do piloto |
| S8.1 | Revisão de consistência |

## Cuidados

- Nunca envie fotos reais da criança ao Canva AI. Insira a foto à mão, só na cópia da família.
- Os pictogramas da rotina devem vir do ARASAAC ou de um único conjunto de ícones do Canva, nunca gerados por IA.
- Se o resultado sair em inglês, use: "Translate all text in this design to Brazilian Portuguese, keeping the layout."
