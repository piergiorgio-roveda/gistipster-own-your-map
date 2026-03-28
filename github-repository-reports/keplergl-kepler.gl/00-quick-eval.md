# Quick Eval: keplergl/kepler.gl

**Data:** 2026-03-26 **Modello:** gemini-3.1-pro-preview **Data Summary:** 01-data-summary.md

---

### Sintesi

Kepler.gl è uno strumento geospaziale open source maturo e altamente popolare per l'analisi visiva
di dataset su larga scala, basato su TypeScript.

### Punti di Forza

- **Adozione massiva:** Straordinaria validazione da parte della community con oltre 11.600 star e
  1.900 fork.
- **Licenza enterprise-friendly:** Rilasciato sotto licenza MIT, garantisce massima flessibilità per
  l'integrazione commerciale.
- **Manutenzione attiva:** Rilasci costanti e recenti (versione v3.2.6 rilasciata a marzo 2026) con
  commit aggiornati agli ultimi giorni.
- **Stack moderno:** L'utilizzo di TypeScript favorisce la robustezza e la manutenibilità in
  integrazioni complesse.

### Rischi e Criticità

- **Bus Factor critico:** Con un valore pari a 2, i primi due contributor (@igorDykhta e
  @heshan0131) accentrano quasi il 73% dello sviluppo storico, ponendo un serio rischio di
  continuità.
- **Backlog oneroso:** La presenza di 610 issue aperte indica un potenziale collo di bottiglia nella
  risoluzione dei bug o nella gestione delle richieste della community.
- **Velocità di sviluppo ridotta:** Solo 10 commit negli ultimi 90 giorni suggeriscono che il
  progetto si trovi in una fase di mantenimento a bassa intensità piuttosto che di evoluzione
  attiva.

### Raccomandazione

**Valutare con cautela** Nonostante l'eccellente popolarità e la stabilità apparente, la forte
dipendenza da soli due sviluppatori chiave e l'ampio backlog di issue richiedono un piano di
mitigazione prima di adottarlo come dipendenza architetturale critica.

### Punteggio

**3.8 / 5.0** — Progetto leader di mercato e funzionalmente solido, ma penalizzato da metriche di
governance (Bus Factor) e gestione community (Issue) non ottimali.

---

## ⚠️ Nota sulla Generazione del Contenuto

Questo report è stato generato in parte o nella sua totalità da un sistema di intelligenza
artificiale (LLM: gemini-3.1-pro-preview).

- **Dati di input**: Metadati, commit, issue e metriche raccolte deterministicamente dalle API
  GitHub
- **Analisi qualitativa**: Generata dall'LLM basandosi esclusivamente sui dati sopra indicati
- **Verifica richiesta**: Le valutazioni e conclusioni dovrebbero essere verificate da un revisore
  umano prima di essere utilizzate per decisioni critiche
