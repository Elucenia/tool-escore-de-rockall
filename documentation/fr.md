<!-- ELUCENIA technical documentation · escore-de-rockall · fr · no clinical/professional/rights approval -->

# Score de Rockall

[conditions, sources et autorisations](https://elucenia.org/fr/outils/escore-de-rockall)

## Mode d’emploi

Utilisez l’outil sur le portail ou ouvrez index.html via un serveur HTTP local. Sélectionnez la langue, remplissez les champs et lancez le calcul.

## Données d’entrée et unités

### Âge

`idade`

- `0` — \< 60 ans
- `1` — 60 à 79 ans
- `2` — ≥ 80 ans

### Choc

`choque`

- `0` — Sans état de choc (pression artérielle systolique ≥ 100 et fréquence cardiaque \< 100)
- `1` — Tachycardie (pression artérielle systolique ≥ 100 et fréquence cardiaque ≥ 100)
- `2` — Hypotension (pression artérielle systolique \< 100 mmHg)

### Comorbidités

`comorb`

- `0` — Aucune importante
- `2` — Insuffisance cardiaque, cardiopathie ischémique ou autre comorbidité importante
- `3` — Insuffisance rénale, insuffisance hépatique ou cancer disséminé

### Diagnostic endoscopique

`diag`

- `0` — Mallory-Weiss ou absence de lésion (sans stigmates)
- `1` — Tous les autres diagnostics
- `2` — Néoplasie du tube digestif supérieur
- `na` — Endoscopie non encore réalisée

### Stigmates d’hémorragie récente

`estigma`

- `0` — Aucun ou tache sombre seule (hématine)
- `2` — Sang dans le tube digestif supérieur, caillot adhérent, vaisseau visible ou saignement en jet
- `na` — Endoscopie non encore réalisée

## Édition de la méthode

Rockall 1996 : préendoscopique 0–7 et complet 0–11 ; distinct du GBS

## Formule documentée

Préendoscopique (0 à 7) : âge (0 à 2) + choc (0 à 2) + comorbidités (0, 2 ou 3).

Complet (0 à 11) : ajoute le diagnostic (0 à 2) et les stigmates d’hémorragie récente (0 ou 2).

## Limites et population

Le Rockall de 1996 a été étudié chez des personnes de plus de 16 ans présentant une hémorragie digestive haute aiguë. La version complète dépend du diagnostic et des stigmates endoscopiques ; la version préendoscopique ne contient pas cette information. La stratification aide à envisager la prise en charge, mais ne détermine pas individuellement la sécurité d’une sortie ou l’absence de récidive hémorragique.

## Références

- [Rockall TA et al. Risk assessment after acute upper gastrointestinal haemorrhage. Gut, 1996.](https://doi.org/10.1136/gut.38.3.316)

- [Stanley AJ et al. Comparison of risk scoring systems for patients presenting with upper gastrointestinal bleeding: international multicentre prospective study. BMJ, 2017.](https://doi.org/10.1136/bmj.i6432)

## Reproduire les tests techniques

Exécutez node test.cjs dans le répertoire racine de ce dépôt pour reproduire les cas synthétiques enregistrés. Les données d’entrée, les résultats attendus et les tolérances d’origine sont conservés. Les tests techniques ne constituent pas une validation clinique.

```sh
node test.cjs
```

tool.json contient les sources, l’édition et le périmètre de la revue. examples.json conserve les données d’entrée et les résultats attendus des cas synthétiques ; results.json consigne les résultats obtenus.

[Fiche et références](../tool.json) · [Code JavaScript](../calculator.js) · [Cas de référence](../examples.json) · [results.json](../results.json)

## Revue et conditions d’utilisation

Aucune révision clinique indépendante n’a été effectuée.

Cette interface est une traduction réalisée par nos soins, et non une édition officielle ou certifiée. La revue clinique indépendante, la révision linguistique professionnelle et l’autorisation des droits sur les instruments n’ont pas été réalisées.

Résultat de la formule ou de la classification. L’interprétation, la conduite et l’applicabilité dépendent de l’évaluation professionnelle et de la source sélectionnée.

## Licence et attribution

Apache-2.0 s’applique uniquement au code d’ELUCENIA. Les droits sur les instruments, publications, traductions et données restent ceux de leurs titulaires respectifs. Conservez LICENSE et NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Résultats documentés

Les informations ci-dessous conservent les sorties de la méthode pour des exemples synthétiques. Elles ne constituent pas une validation clinique indépendante.

### 1

Rockall pré-endoscopique 0 : faible risque

Complétez avec le diagnostic et les stigmates après l’endoscopie pour le score complet.


### 2

Rockall pré-endoscopique ≥ 4 : risque accru de décès

Complétez avec le diagnostic et les stigmates après l’endoscopie pour le score complet.


### 3

Rockall complet ≤ 2 : faible risque de resaignement et de décès

| Détails du résultat | |
| --- | --- |
| Partie pré-endoscopique | 1 points |


### 4

Rockall complet de 3 à 4 : risque intermédiaire

| Détails du résultat | |
| --- | --- |
| Partie pré-endoscopique | 4 points |


### 5

Rockall complet ≥ 5 : risque élevé de décès

| Détails du résultat | |
| --- | --- |
| Partie pré-endoscopique | 7 points |

