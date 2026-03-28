# Quick Eval: geostreams/geodashboard

**Data:** 2026-03-27 **Modello:** gemini-3.1-pro-preview **Data Summary:** 01-data-summary.md

---

### Sintesi

Un frontend JavaScript specifico per le API Geostreams, caratterizzato da una base di contributori
storicamente ben distribuita ma attualmente in evidente stato di stallo e con un'adozione pubblica
quasi nulla.

### Punti di Forza

- **Resilienza del team storico:** Un Bus Factor di 4 su 10 contributori totali indica che la
  conoscenza del progetto era ben distribuita e non legata a un singolo sviluppatore.
- **Maturità delle release passate:** Il raggiungimento della versione v3.9.5 con 10 release totali
  dimostra che il software ha superato le fasi iniziali di prototipazione.

### Rischi e Criticità

- **Sviluppo inattivo:** Nessun commit negli ultimi 90 giorni, ultimo aggiornamento del codice a
  ottobre 2024 e ultima release ferma a luglio 2023 (quasi tre anni fa rispetto alla data di
  valutazione).
- **Adozione inesistente:** Metriche di community estremamente basse (3 stars, 1 fork) suggeriscono
  che si tratti di uno strumento di nicchia o ad uso puramente interno, privo di validazione da
  parte della community GIS.
- **Debito manutentivo:** La presenza di 15 issue aperte a fronte di uno sviluppo fermo indica
  problemi o richieste non risolte che difficilmente troveranno supporto a breve.

### Raccomandazione

**Evitare** Il progetto risulta di fatto abbandonato e privo di una community attiva. A meno che non
sia un requisito architetturale obbligatorio per interfacciarsi con un'infrastruttura Geostreams
legacy già in uso, il rischio di obsolescenza (particolarmente critico nell'ecosistema JavaScript) è
troppo elevato per giustificarne l'adozione.

### Punteggio

**1.5 / 5.0** — Progetto storicamente strutturato ma fortemente penalizzato dall'assenza di
manutenzione recente e dalla totale mancanza di trazione open source.

---

## ⚠️ Nota sulla Generazione del Contenuto

Questo report è stato generato in parte o nella sua totalità da un sistema di intelligenza
artificiale (LLM: gemini-3.1-pro-preview).

- **Dati di input**: Metadati, commit, issue e metriche raccolte deterministicamente dalle API
  GitHub
- **Analisi qualitativa**: Generata dall'LLM basandosi esclusivamente sui dati sopra indicati
- **Verifica richiesta**: Le valutazioni e conclusioni dovrebbero essere verificate da un revisore
  umano prima di essere utilizzate per decisioni critiche
