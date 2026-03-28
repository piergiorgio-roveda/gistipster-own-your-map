# Quick Eval: pip-install-python/dash-dynamic-grid-layout

**Data:** 2026-03-27 **Modello:** gemini-3.1-pro-preview **Data Summary:** 01-data-summary.md

---

### Sintesi

Libreria di componenti UI per Dash applicabile alla creazione di dashboard geospaziali interattive,
ma caratterizzata da un'adozione marginale e da uno sviluppo attualmente stagnante.

### Punti di Forza

- **Licenza permissiva:** Rilasciato sotto licenza MIT, ideale per l'integrazione senza vincoli in
  stack GIS commerciali o proprietari.
- **Rischio chiave mitigato:** Nonostante le dimensioni ridotte, il progetto ha un Bus Factor di 3,
  con un carico di lavoro ben distribuito tra i contributori (nessuno supera il 51% dei commit).
- **Zero issue aperte:** Nessun bug o problema attualmente pendente sul tracker (sebbene questo sia
  probabilmente correlato alla scarsa adozione).

### Rischi e Criticità

- **Sviluppo inattivo:** Il progetto è fermo, con zero commit negli ultimi 90 giorni e l'ultima
  modifica risalente ad aprile 2025.
- **Maturità limitata:** Esiste una sola release pubblicata (agosto 2024), il che suggerisce un
  progetto rimasto allo stadio di Proof of Concept.
- **Scarsa adozione:** Metriche di community estremamente basse (26 star, 3 fork, 1 watcher),
  indicando assenza di trazione e di test sul campo da parte di terzi.
- **Nessuna funzionalità GIS nativa:** Essendo un componente UI generico, richiede lavoro di
  integrazione aggiuntivo per ospitare mappe o widget geospaziali complessi.

### Raccomandazione

**Evitare** Il progetto risulta di fatto abbandonato e privo di una community attiva; per le
dashboard GIS in Python è più sicuro affidarsi ai layout manager nativi di Dash/Plotly o a librerie
UI con manutenzione costante.

### Punteggio

**1.5 / 5.0** — Ottima licenza e buona distribuzione iniziale dei contributi, ma pesantemente
penalizzato dall'abbandono dello sviluppo e dall'assenza di adozione reale.

---

## ⚠️ Nota sulla Generazione del Contenuto

Questo report è stato generato in parte o nella sua totalità da un sistema di intelligenza
artificiale (LLM: gemini-3.1-pro-preview).

- **Dati di input**: Metadati, commit, issue e metriche raccolte deterministicamente dalle API
  GitHub
- **Analisi qualitativa**: Generata dall'LLM basandosi esclusivamente sui dati sopra indicati
- **Verifica richiesta**: Le valutazioni e conclusioni dovrebbero essere verificate da un revisore
  umano prima di essere utilizzate per decisioni critiche
