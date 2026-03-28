---
repo: nkarasiak/qgis-mcp
url: https://github.com/nkarasiak/qgis-mcp
date_analysis: 2026-03-26
version: 1
analyst: pipeline/report-builder
status: draft
---

# nkarasiak/qgis-mcp — Valutazione Tecnica

> **Repository**: [nkarasiak/qgis-mcp](https://github.com/nkarasiak/qgis-mcp) | **Data analisi**:
> 2026-03-26 | **Versione**: 1

---

## Indice

| #   | Sezione               | Disponibilità    |
| --- | --------------------- | ---------------- |
| 1   | Quick Summary         | obbligatoria     |
| 2   | Informazioni Generali | obbligatoria     |
| 3   | Attività di Sviluppo  | dati disponibili |
| 5   | Release               | dati disponibili |
| 8   | Issues & PR           | dati disponibili |
| A1  | Analisi LLM           | allegato         |

---

## Quick Summary

| Indicatore | Status    | Note                                                    |
| ---------- | --------- | ------------------------------------------------------- |
| Salute     | 🟡 5.6/10 | score composito (attività + BF + issue + release + sec) |
| Attività   | 🟢 Attivo | ultimo commit: 2026-03-16                               |
| Bus Factor | 🔴 0      | contributor dominanti                                   |
| Sicurezza  | ⚪ N/D    | OpenSSF Scorecard                                       |
| CI/CD      | ⚪ N/D    | da topics repo                                          |
| Community  | ⚪ 18     | ★ stars                                                 |

---

## 1. Informazioni Generali

| Campo       | Valore                                                                     |
| ----------- | -------------------------------------------------------------------------- |
| Repository  | [nkarasiak/qgis-mcp](https://github.com/nkarasiak/qgis-mcp)                |
| Categoria   | Backend                                                                    |
| Licenza     | —                                                                          |
| Linguaggio  | Python                                                                     |
| Stars       | 18                                                                         |
| Forks       | 4                                                                          |
| Watchers    | 3                                                                          |
| Open Issues | 1                                                                          |
| Creato      | 2026-03-11 (1 mese fa)                                                     |
| Archivio    | No                                                                         |
| Fork        | No                                                                         |
| PyPI        | [https://pypi.org/project/qgis-mcp](https://pypi.org/project/qgis-mcp)     |
| DeepWiki    | [deepwiki.com/nkarasiak/qgis-mcp](https://deepwiki.com/nkarasiak/qgis-mcp) |

---

## 3. Attività di Sviluppo

| Metrica            | Valore              |
| ------------------ | ------------------- |
| Ultimo commit      | 2026-03-16          |
| Commit (30 giorni) | 10                  |
| Commit (90 giorni) | 10                  |
| Trend commit       | ↑ In crescita       |
| Ultima release     | v0.2.1 (2026-03-16) |

---

## 5. Release

| Metrica             | Valore     |
| ------------------- | ---------- |
| Totale release      | 6          |
| Ultima release      | v0.2.1     |
| Data ultima release | 2026-03-16 |

---

## 8. Issues & PR

| Metrica             | Valore |
| ------------------- | ------ |
| Issue aperte        | 1      |
| Issue chiuse (90gg) | 0      |

---

## A1 — Analisi LLM

> _Generata da `pipeline analyze` — fonte: `01-analysis/llm-analysis.md`_

# LLM Analysis: nkarasiak/qgis-mcp

**Data:** 2026-03-26 **Sezione:** all **Modello:** gemini-3.1-pro-preview **Data Summary:**
01-data-summary.md

---

Ecco l'analisi tecnica del repository `nkarasiak/qgis-mcp` basata esclusivamente sui metadati
forniti.

## Sintesi del Progetto

Il progetto è un'integrazione estremamente recente (creata l'11 marzo 2026) che funge da bridge tra
il software desktop QGIS e l'intelligenza artificiale Claude di Anthropic, utilizzando il Model
Context Protocol (MCP). Si trova in una fase di _rapid prototyping_ o _Proof of Concept_ (PoC).

---

## 1. ARCHITETTURA

### Stack Tecnologico e Pattern

- **Linguaggio:** Python (standard de facto per lo scripting e lo sviluppo di plugin in QGIS).
- **Pattern Architetturale (Inferito):** Il progetto implementa un pattern di tipo _Adapter_ o
  _Bridge_. Utilizzando il Model Context Protocol (MCP), disaccoppia l'interfaccia client (QGIS) dal
  provider del modello LLM (Claude).
- **Integrazione GIS:** Essendo destinato a QGIS, è altamente probabile che l'architettura si
  interfacci con le librerie PyQGIS per l'estrazione del contesto spaziale e dei metadati dei layer
  da inviare al modello.

### Valutazione Scalabilità e Manutenibilità

- **Pro:** L'adozione dello standard MCP è una scelta architetturale eccellente. MCP standardizza il
  modo in cui le applicazioni forniscono contesto ai foundation model, rendendo l'architettura
  potenzialmente agnostica rispetto al provider LLM futuro (scalabilità orizzontale verso altri
  modelli).
- **Contro:** Con soli 10 commit totali, l'architettura è presumibilmente monolitica e focalizzata
  sul Minimum Viable Product (MVP).

> ⚠️ **Finding Architetturale:** Il progetto è nelle sue primissime fasi di vita (15 giorni dalla
> creazione). L'architettura attuale è probabilmente ottimizzata per la validazione dell'idea
> piuttosto che per la manutenibilità a lungo termine.

**Raccomandazioni:**

- Strutturare il codice fin da ora separando nettamente la logica di interfaccia utente (QGIS GUI),
  la logica di estrazione dati (PyQGIS) e il client MCP.

---

## 2. SICUREZZA

### Analisi OpenSSF e Processi

- **OpenSSF Scorecard:** `[DATO MANCANTE]` - Non sono forniti dati relativi a scansioni di sicurezza
  automatizzate.
- **Processi di Security:** `[DATO MANCANTE]` - Non ci sono evidenze di policy di sicurezza (es.
  `SECURITY.md`).

### Rischi Identificati (Domain-Specific)

Data la natura del progetto (connessione di un GIS locale a un LLM cloud), emergono specifici
vettori di rischio:

1. **Gestione dei Segreti:** Necessità di gestire in modo sicuro le API Key di Anthropic/Claude
   all'interno dell'ambiente QGIS.
2. **Data Exfiltration / Privacy:** Rischio di invio accidentale di dati geospaziali sensibili o
   proprietari (es. attributi di layer vettoriali, percorsi file locali) ai server di Anthropic come
   "contesto" per il modello.
3. **Esecuzione di Codice Arbitrario:** Se il plugin permette a Claude di generare ed eseguire
   script Python o query SQL (PostGIS) direttamente in QGIS, esiste un grave rischio di _Prompt
   Injection_ che potrebbe compromettere il sistema locale.

**Raccomandazioni:**

- Implementare un meccanismo di _Data Masking_ o un sistema di opt-in esplicito prima di inviare i
  metadati dei layer GIS al cloud.
- Assicurarsi che le API key siano salvate utilizzando il QGIS Authentication Manager
  (QgsAuthManager) e non in file di testo in chiaro.
- Se è prevista l'esecuzione di codice generato dall'AI, implementare una sandbox rigorosa o
  richiedere sempre l'approvazione manuale dell'utente (Human-in-the-loop).

---

## 3. QUALITÀ

### Metriche di Sviluppo e Maturità

| Metrica               | Valore            | Analisi                                                                           |
| :-------------------- | :---------------- | :-------------------------------------------------------------------------------- |
| **Età del progetto**  | 15 giorni         | Progetto in fase embrionale (creato 11/03/2026).                                  |
| **Velocity (Commit)** | 10 (ultimi 30gg)  | Attività concentrata nei primissimi giorni di vita.                               |
| **Frequenza Rilasci** | 6 release in 5 gg | Altissima frequenza. Indica un approccio _trial-and-error_ o _rapid prototyping_. |
| **Versione Attuale**  | v0.2.1            | Coerente con lo stato di pre-produzione (Major version 0).                        |

### Contributor e Gestione Community

- **Bus Factor:** `[DATO MANCANTE]` sul numero esatto di contributor, ma dato il nome del repository
  (`nkarasiak`) e il basso numero di commit, è altamente probabile che il Bus Factor sia pari a
  **1** (single-maintainer project).
- **Traction:** 18 Stars e 4 Forks in 15 giorni indicano un discreto interesse organico iniziale da
  parte della community GIS/AI per questo specifico use-case.
- **Gestione Issue:** 1 Open Issue. Non ci sono dati sui tempi di risoluzione, ma la presenza di
  issue aperti indica che gli utenti stanno iniziando a testare il tool.

> ⚠️ **Finding Qualitativo:** Il rapporto tra commit (10) e release (6) è anomalo (quasi una release
> ogni 1.6 commit). Questo suggerisce l'assenza di una pipeline CI/CD strutturata e un processo di
> rilascio manuale e frammentato, tipico dei progetti appena nati.

**Raccomandazioni:**

- **Stabilizzazione:** Rallentare il ciclo di rilascio. Raggruppare le feature e i bugfix in release
  più corpose per evitare "release fatigue" negli utenti QGIS.
- **Automazione:** Implementare GitHub Actions per il linting del codice Python (es. `flake8`,
  `black`) e per la pacchettizzazione automatica del plugin QGIS ad ogni tag di release.
- **Documentazione:** Dato l'interesse iniziale (18 stars in 2 settimane), è cruciale fornire un
  `README.md` dettagliato che spieghi i prerequisiti (es. installazione di server MCP) e i limiti
  attuali del PoC.

---

## ⚠️ Nota sulla Generazione del Contenuto

Questo report è stato generato in parte o nella sua totalità da un sistema di intelligenza
artificiale (LLM: gemini-3.1-pro-preview).

- **Dati di input**: Metadati, commit, issue e metriche raccolte deterministicamente dalle API
  GitHub
- **Analisi qualitativa**: Generata dall'LLM basandosi esclusivamente sui dati sopra indicati
- **Verifica richiesta**: Le valutazioni e conclusioni dovrebbero essere verificate da un revisore
  umano prima di essere utilizzate per decisioni critiche

---
