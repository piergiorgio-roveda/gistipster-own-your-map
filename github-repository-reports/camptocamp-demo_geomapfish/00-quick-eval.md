# Quick Eval: camptocamp/demo_geomapfish

**Data:** 2026-03-26 **Modello:** gemini-3.1-pro-preview **Data Summary:** 01-data-summary.md

---

### Sintesi

Repository dimostrativo storico per l'ecosistema GeoMapFish, mantenuto attivamente ma utilizzato
prevalentemente come template o ambiente di test interno piuttosto che come strumento standalone per
la community.

### Punti di Forza

- **Longevità e supporto continuo:** Creato nel 2012, registra commit recentissimi (marzo 2026),
  dimostrando una manutenzione costante nel tempo.
- **Licenza enterprise-friendly:** Rilasciato sotto BSD-2-Clause, garantisce massima libertà di
  utilizzo e modifica.
- **Utilità pratica:** Il numero di fork (15) superiore a quello delle star (7) suggerisce un
  utilizzo concreto come base di partenza o scaffolding per progetti derivati.
- **Automazione presente:** La presenza di un bot CI dedicato (`@c2c-bot-gis-ci`) indica l'esistenza
  di pipeline di test/deploy automatizzate.

### Rischi e Criticità

- **Centralizzazione estrema (Key Person Risk):** Bus Factor pari a 2, con un singolo sviluppatore
  (`@sbrunner`) responsabile di quasi il 70% dei commit storici (oltre 2100 contributi).
- **Scarsa trazione pubblica:** Solo 7 star in 14 anni di vita indicano che il progetto non ha una
  vera e propria community esterna attiva.
- **Sviluppo a bassa intensità:** Solo 10 commit negli ultimi 90 giorni, indicativi di una fase di
  pura manutenzione ordinaria.
- **Accoppiamento tecnologico:** Il linguaggio principale (PLpgSQL) suggerisce una forte dipendenza
  logica dal livello database (PostgreSQL/PostGIS).

### Raccomandazione

**Valutare con cautela** Essendo un progetto puramente dimostrativo e fortemente dipendente da un
singolo maintainer, è eccellente come _reference implementation_ per comprendere le architetture
GeoMapFish, ma non deve essere trattato o integrato come una dipendenza software critica in
produzione.

### Punteggio

**2.5 / 5.0** — Progetto longevo e aggiornato, ma fortemente penalizzato dal Bus Factor critico e
dalla sua natura di "demo" a uso prevalentemente interno.

---

## ⚠️ Nota sulla Generazione del Contenuto

Questo report è stato generato in parte o nella sua totalità da un sistema di intelligenza
artificiale (LLM: gemini-3.1-pro-preview).

- **Dati di input**: Metadati, commit, issue e metriche raccolte deterministicamente dalle API
  GitHub
- **Analisi qualitativa**: Generata dall'LLM basandosi esclusivamente sui dati sopra indicati
- **Verifica richiesta**: Le valutazioni e conclusioni dovrebbero essere verificate da un revisore
  umano prima di essere utilizzate per decisioni critiche
