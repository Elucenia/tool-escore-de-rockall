<!-- ELUCENIA technical documentation · escore-de-rockall · it · no clinical/professional/rights approval -->

# Punteggio di Rockall

[condizioni, fonti e autorizzazioni](https://elucenia.org/it/strumenti/escore-de-rockall)

## Come usare

Usi lo strumento nel portale oppure apra index.html tramite un server HTTP locale. Selezioni la lingua, compili i campi ed esegua il calcolo.

## Dati di ingresso e unità

### Età

`idade`

- `0` — \< 60 anni
- `1` — 60 a 79 anni
- `2` — ≥ 80 anni

### Shock

`choque`

- `0` — Nessuno shock (pressione arteriosa sistolica ≥ 100 e frequenza cardiaca \< 100)
- `1` — Tachicardia (pressione arteriosa sistolica ≥ 100 e frequenza cardiaca ≥ 100)
- `2` — Ipotensione (pressione arteriosa sistolica \< 100 mmHg)

### Comorbilità

`comorb`

- `0` — Nessuna importante
- `2` — Insufficienza cardiaca, cardiopatia ischemica o altra comorbilità importante
- `3` — Insufficienza renale, insufficienza epatica o cancro disseminato

### Diagnosi endoscopica

`diag`

- `0` — Mallory-Weiss o nessuna lesione (senza stigmate)
- `1` — Tutte le altre diagnosi
- `2` — Neoplasia del tratto digestivo superiore
- `na` — Endoscopia non ancora eseguita

### Stigmate di sanguinamento recente

`estigma`

- `0` — Nessuna o solo macchia scura (ematina)
- `2` — Sangue nel tratto superiore, coagulo aderente, vaso visibile o sanguinamento a getto
- `na` — Endoscopia non ancora eseguita

## Edizione del metodo

Rockall 1996: preendoscopico 0–7 e completo 0–11; distinto dal GBS

## Formula documentata

Preendoscopico (da 0 a 7): età (da 0 a 2) + shock (da 0 a 2) + comorbilità (0, 2 o 3).

Completo (da 0 a 11): aggiunge diagnosi (da 0 a 2) e stigmate di sanguinamento recente (0 o 2).

## Limiti e popolazione

Il Rockall del 1996 è stato studiato in persone di età superiore a 16 anni con emorragia digestiva alta acuta. La versione completa dipende dalla diagnosi e dalle stigmate endoscopiche; quella pre-endoscopica non contiene queste informazioni. La stratificazione aiuta a considerare la gestione, ma non determina la sicurezza individuale della dimissione o l’assenza di risanguinamento.

## Riferimenti

- [Rockall TA et al. Risk assessment after acute upper gastrointestinal haemorrhage. Gut, 1996.](https://doi.org/10.1136/gut.38.3.316)

- [Stanley AJ et al. Comparison of risk scoring systems for patients presenting with upper gastrointestinal bleeding: international multicentre prospective study. BMJ, 2017.](https://doi.org/10.1136/bmj.i6432)

## Riprodurre i test tecnici

Esegua node test.cjs nella cartella principale di questo repository per ripetere i casi sintetici registrati. Gli input, i risultati attesi e le tolleranze originali sono conservati. I test tecnici non costituiscono validazione clinica.

```sh
node test.cjs
```

tool.json contiene le fonti, l’edizione e l’ambito della revisione. examples.json conserva gli input e i risultati attesi dei casi sintetici; results.json registra i risultati ottenuti.

[Scheda e riferimenti](../tool.json) · [Codice JavaScript](../calculator.js) · [Casi di riferimento](../examples.json) · [results.json](../results.json)

## Revisione e condizioni d’uso

Non è stata effettuata una revisione clinica indipendente.

Questa interfaccia è una traduzione realizzata dagli autori, non un’edizione ufficiale o certificata. Non sono state eseguite la revisione clinica indipendente, la revisione linguistica professionale né la verifica delle autorizzazioni relative ai diritti sugli strumenti.

Risultato della formula o classificazione. Interpretazione, condotta e applicabilità dipendono dalla valutazione professionale e dalla fonte selezionata.

## Licenza e attribuzione

Apache-2.0 si applica solo al codice di ELUCENIA. I diritti su strumenti, pubblicazioni, traduzioni e dati restano ai rispettivi titolari. Conservi LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026
