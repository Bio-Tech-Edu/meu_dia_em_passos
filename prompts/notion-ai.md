# Notion AI: instruções e prompts

**Função no projeto:** manter o Mapa de preferências alimentares (template "Food Chaining – versão minimalista") e as fichas de acompanhamento em formato de base de dados.
**Template original:** [Mapa de preferências alimentares](https://pamellabiotech.notion.site/MAPA-DE-PREFER-NCIAS-ALIMENTARES-2f106a06ea8280129577d4d0f07fcce9)

## Boas práticas

1. **Duplique** o template antes de pedir qualquer mudança à IA e mantenha o original intacto.
2. A cópia com dados reais da família fica **privada** e não é publicada na web.
3. Para testes e exemplos, use apenas a "Criança A".

## Prompts deste projeto

| ID | Uso |
|---|---|
| S4.1 | Gerar a versão do planner (9A Meus alimentos e 9B Cadeia alimentar) |
| S4.2 | Preencher um exemplo fictício de 6 semanas |

## Prompt extra: transformar em base de dados

```text
Transforme a tabela "Alimentos aceitos" desta página em uma base de dados com as propriedades:
Alimento (título), Marca (texto), Sabor (seleção: Doce, Salgado, Azedo, Amargo, Picante, Neutro),
Textura (multisseleção: Crocante, Macia, Seca, Pegajosa, Mastigável, Dura, Úmida), Visual (texto), Notas (texto).
Crie também uma visualização em galeria agrupada por Textura.
```

## Prompt extra: resumo semanal

```text
Com base nos registros desta semana na tabela "Progressão", escreva um resumo de até 5 tópicos para levar ao profissional:
o que mudou, o resultado (olhou, tocou, provou, aceitou), padrões percebidos e 2 perguntas para o profissional.
Não faça recomendações clínicas.
```
