# Quick Eval: maplibre/maplibre-gl-js

**Data:** 2026-03-26 **Modello:** gemini-3.1-pro-preview **Data Summary:** 01-data-summary.md

---

### Sintesi

MapLibre GL JS è una libreria TypeScript di riferimento nel panorama open source per il rendering di
mappe vettoriali web, caratterizzata da un'altissima adozione ma con metriche di sviluppo recenti
che richiedono attenzione.

### Punti di Forza

- **Adozione massiva:** Con oltre 10.000 star e più di 1.000 fork, il progetto gode di un'eccellente
  validazione da parte della community GIS.
- **Stack tecnologico solido:** L'uso di TypeScript garantisce maggiore robustezza, tipizzazione e
  manutenibilità per integrazioni enterprise.
- **Release management attivo:** Nonostante un basso volume di commit, il progetto è attivamente
  pacchettizzato e distribuito (ultima release v5.21.1 rilasciata a ridosso dell'analisi).
- **Storico contributori:** La base di codice beneficia dell'impronta di sviluppatori storici e
  altamente specializzati nel web mapping vettoriale.

### Rischi e Criticità

- **Ambiguità legale:** Il metadato della licenza riporta "NOASSERTION", rendendo obbligatoria una
  due-diligence legale prima di qualsiasi integrazione commerciale.
- **Rallentamento dello sviluppo:** Solo 10 commit negli ultimi 90 giorni (tutti concentrati negli
  ultimi 30), un volume anomalo e molto basso per un progetto di questa portata.
- **Accumulo di issue:** Le 412 issue aperte, confrontate con il basso rateo di commit recenti,
  suggeriscono una potenziale difficoltà del team nel gestire il triage e la risoluzione dei bug.
- **Bus Factor limitato:** Un valore pari a 4 indica che la conoscenza critica del progetto è
  concentrata in un nucleo molto ristretto di maintainer.

### Raccomandazione

**Valutare con cautela** Sebbene sia uno standard _de facto_ per il web mapping vettoriale,
l'anomalia sui metadati della licenza e il drastico calo dei commit recenti a fronte di molte issue
aperte richiedono un'attenta valutazione prima di legare architetture critiche a questa specifica
versione.

### Punteggio

**3.8 / 5.0** — Progetto leader per popolarità e utilità, ma penalizzato dall'incertezza sulla
licenza e da metriche di manutenzione recente sottotono.

---

## ⚠️ Nota sulla Generazione del Contenuto

Questo report è stato generato in parte o nella sua totalità da un sistema di intelligenza
artificiale (LLM: gemini-3.1-pro-preview).

- **Dati di input**: Metadati, commit, issue e metriche raccolte deterministicamente dalle API
  GitHub
- **Analisi qualitativa**: Generata dall'LLM basandosi esclusivamente sui dati sopra indicati
- **Verifica richiesta**: Le valutazioni e conclusioni dovrebbero essere verificate da un revisore
  umano prima di essere utilizzate per decisioni critiche
