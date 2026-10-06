<!-- ELUCENIA technical documentation · escore-de-rockall · es · no clinical/professional/rights approval -->

# Puntuación de Rockall

[condiciones, fuentes y permisos](https://elucenia.org/es/herramientas/escore-de-rockall)

## Cómo usar

Utilice la herramienta en el portal o abra index.html mediante un servidor HTTP local. Seleccione el idioma, complete los campos y calcule.

## Entradas y unidades

### Edad

`idade`

- `0` — \< 60 años
- `1` — 60 a 79 años
- `2` — ≥ 80 años

### Shock

`choque`

- `0` — Sin choque (presión arterial sistólica ≥ 100 y frecuencia cardíaca \< 100)
- `1` — Taquicardia (presión arterial sistólica ≥ 100 y frecuencia cardíaca ≥ 100)
- `2` — Hipotensión (presión arterial sistólica \< 100 mmHg)

### Comorbilidades

`comorb`

- `0` — Ninguna importante
- `2` — Insuficiencia cardíaca, cardiopatía isquémica u otra comorbilidad importante
- `3` — Insuficiencia renal, insuficiencia hepática o cáncer diseminado

### Diagnóstico endoscópico

`diag`

- `0` — Mallory-Weiss o ninguna lesión (sin estigmas)
- `1` — Todos los demás diagnósticos
- `2` — Neoplasia del tracto digestivo superior
- `na` — Endoscopia aún no realizada

### Estigmas de sangrado reciente

`estigma`

- `0` — Ninguno o solo mancha oscura (hematina)
- `2` — Sangre en el tracto superior, coágulo adherido, vaso visible o sangrado a chorro
- `na` — Endoscopia aún no realizada

## Edición del método

Rockall 1996: preendoscópico 0–7 y completo 0–11; sin confusión con GBS

## Fórmula documentada

Preendoscópico (0 a 7): edad (0 a 2) + choque (0 a 2) + comorbilidades (0, 2 o 3).

Completo (0 a 11): añade diagnóstico (0 a 2) y estigmas de sangrado reciente (0 o 2).

## Límites y población

El Rockall de 1996 se estudió en personas mayores de 16 años con hemorragia digestiva alta aguda. La versión completa depende del diagnóstico y de los estigmas endoscópicos; la versión preendoscópica no contiene esa información. La estratificación ayuda a considerar el manejo, pero no determina la seguridad individual del alta ni la ausencia de resangrado.

## Referencias

- [Rockall TA et al. Risk assessment after acute upper gastrointestinal haemorrhage. Gut, 1996.](https://doi.org/10.1136/gut.38.3.316)

- [Stanley AJ et al. Comparison of risk scoring systems for patients presenting with upper gastrointestinal bleeding: international multicentre prospective study. BMJ, 2017.](https://doi.org/10.1136/bmj.i6432)

## Reproducir las pruebas técnicas

Ejecute node test.cjs en el directorio raíz de este repositorio para repetir los casos sintéticos registrados. Se conservan las entradas, los resultados esperados y las tolerancias originales. Las pruebas técnicas no constituyen validación clínica.

```sh
node test.cjs
```

tool.json contiene las fuentes, la edición y el alcance de la revisión. examples.json conserva las entradas y los resultados esperados de los casos sintéticos; results.json registra los resultados obtenidos.

[Ficha y referencias](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referencia](../examples.json) · [results.json](../results.json)

## Revisión y condiciones de uso

No se ha realizado una revisión clínica independiente.

Esta interfaz es una traducción de elaboración propia, no una edición oficial o certificada. No se han realizado la revisión clínica independiente, la revisión lingüística profesional ni la autorización de derechos de los instrumentos.

Resultado de la fórmula o clasificación. La interpretación, la conducta y la aplicabilidad dependen de la evaluación profesional y de la fuente seleccionada.

## Licencia y atribución

Apache-2.0 se aplica únicamente al código de ELUCENIA. Los derechos de los instrumentos, publicaciones, traducciones y datos permanecen en manos de sus respectivos titulares. Conserve LICENSE y NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

La información siguiente conserva las salidas del método para ejemplos sintéticos. No constituye una validación clínica independiente.

### 1

Rockall preendoscópico 0: riesgo bajo

Complete con el diagnóstico y los estigmas después de la endoscopia para el puntaje completo.


### 2

Rockall preendoscópico ≥ 4: riesgo aumentado de muerte

Complete con el diagnóstico y los estigmas después de la endoscopia para el puntaje completo.


### 3

Rockall completo ≤ 2: bajo riesgo de resangrado y muerte

| Detalles del resultado | |
| --- | --- |
| Parte preendoscópica | 1 puntos |


### 4

Rockall completo de 3 a 4: riesgo intermedio

| Detalles del resultado | |
| --- | --- |
| Parte preendoscópica | 4 puntos |


### 5

Rockall completo ≥ 5: alto riesgo de muerte

| Detalles del resultado | |
| --- | --- |
| Parte preendoscópica | 7 puntos |

