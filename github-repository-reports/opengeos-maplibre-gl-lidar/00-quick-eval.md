# Quick Eval: opengeos/maplibre-gl-lidar

**Data:** 2026-03-26 **Modello:** gemini-3.1-pro-preview **Data Summary:** 01-data-summary.md

---

### Sintesi

Un plugin TypeScript recente e promettente per l'ecosistema MapLibre, focalizzato sulla
visualizzazione di nuvole di punti LiDAR e distribuito con licenza permissiva.

### Punti di Forza

- **Ottima trazione iniziale:** 174 stelle e 23 fork in soli due mesi e mezzo dalla creazione
  (Gennaio 2026), a dimostrazione di un forte interesse nella community GIS.
- **Stack e licenza aziendali:** Scritto in TypeScript e rilasciato con licenza MIT, garantisce
  facilità di integrazione e zero vincoli legali per l'uso commerciale.
- **Rilasci frequenti:** 10 release pubblicate in un lasso di tempo molto breve, indicando un rapido
  setup iniziale del pacchetto (attualmente alla v0.11.1).

### Rischi e Criticità

- **Bus Factor critico (1):** Il progetto dipende quasi interamente da un singolo sviluppatore
  (@giswqs), autore dell'87.3% dei commit, esponendo il repository a un alto rischio di abbandono.
- **Immaturità del progetto:** Creato a Gennaio 2026 e ancora in versione `0.x.x`, suggerisce che le
  API potrebbero essere instabili e soggette a _breaking changes_.
- **Rallentamento dell'attività:** Un solo commit negli ultimi 30 giorni e nessuna nuova release da
  metà Febbraio 2026, segnale di un possibile stallo dopo lo sprint iniziale.

### Raccomandazione

**Valutare con cautela** Il plugin copre un'esigenza geospaziale specifica (LiDAR su MapLibre) e
mostra un'ottima adozione iniziale, ma l'estrema giovinezza del progetto e la dipendenza totale da
un singolo maintainer lo rendono attualmente troppo rischioso per un'integrazione diretta in
ambienti di produzione _mission-critical_.

### Punteggio

**3.0 / 5.0** — Ottima utilità e trazione iniziale, ma fortemente penalizzato dal Bus Factor pari a
1 e dall'immaturità fisiologica del ciclo di vita.

---

## ⚠️ Nota sulla Generazione del Contenuto

Questo report è stato generato in parte o nella sua totalità da un sistema di intelligenza
artificiale (LLM: gemini-3.1-pro-preview).

- **Dati di input**: Metadati, commit, issue e metriche raccolte deterministicamente dalle API
  GitHub
- **Analisi qualitativa**: Generata dall'LLM basandosi esclusivamente sui dati sopra indicati
- **Verifica richiesta**: Le valutazioni e conclusioni dovrebbero essere verificate da un revisore
  umano prima di essere utilizzate per decisioni critiche
