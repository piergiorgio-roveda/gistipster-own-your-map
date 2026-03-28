# Quick Eval: camptocamp/docker-qgis-server

**Data:** 2026-03-26 **Modello:** gemini-3.1-pro-preview **Data Summary:** 01-data-summary.md

---

### Sintesi

Un'immagine Docker matura per il deployment di QGIS Server, supportata storicamente da un noto
vendor GIS (Camptocamp), ma caratterizzata da una community di adozione estremamente ristretta.

### Punti di Forza

- **Longevità e supporto aziendale:** Progetto attivo dal 2016 sotto l'egida di Camptocamp, garanzia
  di competenza nel dominio geospaziale.
- **Manutenzione costante:** Il repository è attivamente manutenuto, con commit recenti (ultimo a
  marzo 2026).
- **Allineamento versioning:** Le release (es. 3.44.0) seguono la numerazione ufficiale di QGIS,
  facilitando la pianificazione degli aggiornamenti infrastrutturali.
- **Licenza adeguata:** Rilasciato in GPL-2.0, in perfetta conformità con l'ecosistema core di QGIS.

### Rischi e Criticità

- **Key Person Risk estremo:** Nonostante un Bus Factor calcolato a 3, un singolo sviluppatore
  (@sbrunner) concentra il 57% dei commit totali, mentre il secondo umano si ferma all'1.3%.
- **Adozione marginale:** Solo 49 stars e 12 forks in quasi 10 anni di vita indicano che non è lo
  standard de facto della community per containerizzare QGIS Server.
- **Debito tecnico potenziale:** 27 issue aperte sono un numero sproporzionatamente alto rispetto
  alla base utenti ridotta e al basso volume di fork.
- **Latenza nelle release:** L'ultima release ufficiale risale a 9 mesi fa (giugno 2025), nonostante
  vi siano commit recenti, suggerendo possibili ritardi nella pubblicazione di immagini stabili.

### Raccomandazione

**Valutare con cautela** Il progetto è funzionale e mantenuto da esperti del settore, ma l'eccessiva
dipendenza da un singolo maintainer e il backlog di issue aperte richiedono test rigorosi prima di
un'adozione in ambienti di produzione critici.

### Punteggio

**3.0 / 5.0** — Soluzione storicamente affidabile, ma fortemente penalizzata dalla mancanza di una
community attiva e da un evidente collo di bottiglia nello sviluppo umano.

---

## ⚠️ Nota sulla Generazione del Contenuto

Questo report è stato generato in parte o nella sua totalità da un sistema di intelligenza
artificiale (LLM: gemini-3.1-pro-preview).

- **Dati di input**: Metadati, commit, issue e metriche raccolte deterministicamente dalle API
  GitHub
- **Analisi qualitativa**: Generata dall'LLM basandosi esclusivamente sui dati sopra indicati
- **Verifica richiesta**: Le valutazioni e conclusioni dovrebbero essere verificate da un revisore
  umano prima di essere utilizzate per decisioni critiche
