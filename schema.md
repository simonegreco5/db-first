# Database Schema

Modellizzare la struttura di una tabella per memorizzare tutti i dati riguardanti delle auto usate messe in vendita da un concessionario.

## Table name: cars


- id: BIGINT - NOT NULL - UNIQUE
- marca: VARCHAR (30) - NOT NULL
- modello: VARCHAR (30) - NOT NULL
- targa: * VARCHAR (14) - NULL
- prezzo: SMALL - NOT NULL
- condizione: VARCHAR (12) - NOT NULL
- chilometraggio: MEDIUMINT - NOT NULL
- alimentazione: VARCHAR(20) - NOT NULL
- potenza(CV/KWH): SMALL - NOT NULL
- cilindrata: SMALL - NULL
- immatricolazione: CHAR(7) - NOT NULL
- colore: VARCHAR (30) - NULL
- disponibile: VARCHAR (20) - NULL

### note
- targa * se si considera solo il mercato italiano si usa CHAR (7).
- tutti i NOT NULL (fatta eccezione per id) sono stati pensati per una futura ricerca con filtraggio.
- la targa è NULL, in quanto non è indispensabile ai fini dell'acquisto che ci sia già, ci potrebbero essere auto non immatricolate e quindi da targare al momento dell'acquisto.