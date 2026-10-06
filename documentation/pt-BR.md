<!-- ELUCENIA technical documentation · escore-de-rockall · pt-BR · no clinical/professional/rights approval -->

# Escore de Rockall

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/escore-de-rockall)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Idade

`idade`

- `0` — \< 60 anos
- `1` — 60 a 79 anos
- `2` — ≥ 80 anos

### Choque

`choque`

- `0` — Sem choque (PAS ≥ 100 e FC \< 100)
- `1` — Taquicardia (PAS ≥ 100 e FC ≥ 100)
- `2` — Hipotensão (PAS \< 100 mmHg)

### Comorbidades

`comorb`

- `0` — Nenhuma importante
- `2` — Insuficiência cardíaca, cardiopatia isquêmica ou outra comorbidade importante
- `3` — Insuficiência renal, insuficiência hepática ou câncer disseminado

### Diagnóstico endoscópico

`diag`

- `0` — Mallory-Weiss ou nenhuma lesão (sem estigmas)
- `1` — Todos os outros diagnósticos
- `2` — Neoplasia do trato digestivo alto
- `na` — Endoscopia ainda não realizada

### Estigmas de sangramento recente

`estigma`

- `0` — Nenhum ou só ponto escuro (hematina)
- `2` — Sangue no trato alto, coágulo aderido, vaso visível ou em jato
- `na` — Endoscopia ainda não realizada

## Edição do método

Rockall 1996:préendoscópico 0–7 ecompleto 0–11; sem confusão com GBS

## Fórmula documentada

Pré-endoscópico (0 a 7): idade (0 a 2) + choque (0 a 2) + comorbidades (0, 2 ou 3).

Completo (0 a 11): soma também o diagnóstico (0 a 2) e os estigmas de sangramento recente (0 ou 2).

## Limites e população

O Rockall de 1996 foi estudado em pessoas acima de 16 anos com hemorragia digestiva alta aguda. A versão completa depende de diagnóstico e estigmas endoscópicos; a versão pré-endoscópica não contém essa informação. A estratificação ajuda a considerar manejo, mas não determina segurança individual de alta ou ausência de ressangramento.

## Referências

- [Rockall TA et al. Risk assessment after acute upper gastrointestinal haemorrhage. Gut, 1996.](https://doi.org/10.1136/gut.38.3.316)

- [Stanley AJ et al. Comparison of risk scoring systems for patients presenting with upper gastrointestinal bleeding: international multicentre prospective study. BMJ, 2017.](https://doi.org/10.1136/bmj.i6432)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

As informações abaixo preservam as saídas do método para exemplos sintéticos. Não constituem validação clínica independente.

### 1

Rockall pré-endoscópico 0: baixo risco

Complete com o diagnóstico e os estigmas após a endoscopia para o escore completo.


### 2

Rockall pré-endoscópico ≥ 4: risco aumentado de óbito

Complete com o diagnóstico e os estigmas após a endoscopia para o escore completo.


### 3

Rockall completo ≤ 2: baixo risco de ressangramento e óbito

| Detalhes do resultado | |
| --- | --- |
| Parte pré-endoscópica | 1 pontos |


### 4

Rockall completo de 3 a 4: risco intermediário

| Detalhes do resultado | |
| --- | --- |
| Parte pré-endoscópica | 4 pontos |


### 5

Rockall completo ≥ 5: alto risco de óbito

| Detalhes do resultado | |
| --- | --- |
| Parte pré-endoscópica | 7 pontos |

