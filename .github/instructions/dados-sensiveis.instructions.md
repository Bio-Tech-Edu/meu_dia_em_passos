---
applyTo: "**"
---

# Dados sensíveis (LGPD)

Dados de saúde, terapias, alimentação e observações clínicas de criança são dados pessoais sensíveis (Lei nº 13.709/2018).

- Nunca escreva nomes, datas de nascimento, fotos, diagnósticos, nomes de terapeutas, clínicas ou escolas reais.
- Exemplos e testes usam apenas "Criança A", "[NOME]" e `src/data/cartoes.json` com dados fictícios.
- A pasta `/data/` está fora do versionamento: não leia, não crie e não referencie arquivos nela.
- Nada de `fetch`, `XMLHttpRequest`, `navigator.sendBeacon`, WebSocket, analytics ou scripts e fontes externos.
- A persistência acontece apenas em `localStorage`, com prefixo `mdp-` e um botão "Apagar tudo".
- Se encontrar um dado que parece real, pare, avise e sugira substituí-lo por um marcador.
