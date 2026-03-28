# Quick Eval: qgis/QGIS

**Data:** 2026-03-26 **Modello:** gemini-3.1-pro-preview **Data Summary:** 01-data-summary.md

---

### Sintesi

QGIS è il principale sistema informativo geografico (GIS) open source multipiattaforma, consolidato
come standard _de facto_ nel settore grazie alla sua longevità e vasta adozione globale.

### Punti di Forza

- **Adozione massiva:** Oltre 13.400 stars e 3.300 fork confermano il suo ruolo di leader indiscusso
  nel panorama GIS open source.
- **Longevità e stabilità:** Progetto maturo (attivo dal 2011) capace di evolversi fino alla recente
  major release `final-4_0_0` rilasciata a marzo 2026.
- **Core team storico:** Presenza di contributori con migliaia di commit che garantiscono una
  profonda conoscenza del dominio geospaziale e del linguaggio C++.

### Rischi e Criticità

- **Bus Factor critico (1):** Estrema dipendenza da un singolo sviluppatore (@nyalldawson),
  responsabile da solo del 31,2% dei commit totali (quasi 25.000 contribuzioni).
- **Crollo dell'attività recente:** Solo 10 commit negli ultimi 90 giorni; un dato allarmante per un
  progetto di questa scala, specialmente a ridosso di una major release.
- **Backlog di manutenzione:** 5.426 issue aperte indicano un forte sovraccarico dei maintainer e
  probabili colli di bottiglia nella risoluzione di bug e richieste della community.
- **Ecosistema contributori ristretto:** Solo 30 contributori totali registrati nei dati, un numero
  pericolosamente basso per sostenere un repository enterprise di 15 anni.

### Raccomandazione

**Valutare con cautela** Sebbene sia lo standard di mercato assoluto per il GIS desktop, i dati
mostrano un grave rischio di centralizzazione (Bus Factor 1) e un drastico stallo nello sviluppo
recente (10 commit in 3 mesi). L'adozione in contesti mission-critical richiede piani di mitigazione
o supporto commerciale dedicato.

### Punteggio

**3.5 / 5.0** — Leader indiscusso per adozione storica, ma gravemente penalizzato dai parametri di
resilienza del team e dal recente blocco delle attività di sviluppo.

---

## ⚠️ Nota sulla Generazione del Contenuto

Questo report è stato generato in parte o nella sua totalità da un sistema di intelligenza
artificiale (LLM: gemini-3.1-pro-preview).

- **Dati di input**: Metadati, commit, issue e metriche raccolte deterministicamente dalle API
  GitHub
- **Analisi qualitativa**: Generata dall'LLM basandosi esclusivamente sui dati sopra indicati
- **Verifica richiesta**: Le valutazioni e conclusioni dovrebbero essere verificate da un revisore
  umano prima di essere utilizzate per decisioni critiche
