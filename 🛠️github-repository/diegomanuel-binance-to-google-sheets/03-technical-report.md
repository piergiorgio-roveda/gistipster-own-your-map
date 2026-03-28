---
repo: diegomanuel/binance-to-google-sheets
url: https://github.com/diegomanuel/binance-to-google-sheets
date_analysis: 2026-03-27
version: 1
analyst: pipeline/report-builder
status: draft
---

# diegomanuel/binance-to-google-sheets — Valutazione Tecnica

> **Repository**:
> [diegomanuel/binance-to-google-sheets](https://github.com/diegomanuel/binance-to-google-sheets) |
> **Data analisi**: 2026-03-27 | **Versione**: 1

---

## Indice

| #   | Sezione               | Disponibilità    |
| --- | --------------------- | ---------------- |
| 1   | Quick Summary         | obbligatoria     |
| 2   | Informazioni Generali | obbligatoria     |
| 3   | Attività di Sviluppo  | dati disponibili |
| 4   | Contribuenti          | dati disponibili |
| 5   | Release               | dati disponibili |
| 8   | Issues & PR           | dati disponibili |
| A1  | Analisi LLM           | allegato         |

---

## Quick Summary

| Indicatore | Status      | Note                                                    |
| ---------- | ----------- | ------------------------------------------------------- |
| Salute     | 🔴 1.1/10   | score composito (attività + BF + issue + release + sec) |
| Attività   | 🔴 Inattivo | ultimo commit: 2024-02-17                               |
| Bus Factor | 🔴 1        | contributor dominanti                                   |
| Sicurezza  | ⚪ N/D      | OpenSSF Scorecard                                       |
| CI/CD      | ⚪ N/D      | da topics repo                                          |
| Community  | ⚪ 435      | ★ stars                                                 |

---

## 1. Informazioni Generali

| Campo       | Valore                                                                                                           |
| ----------- | ---------------------------------------------------------------------------------------------------------------- |
| Repository  | [diegomanuel/binance-to-google-sheets](https://github.com/diegomanuel/binance-to-google-sheets)                  |
| Categoria   | Frontend                                                                                                         |
| Licenza     | GPL-3.0                                                                                                          |
| Linguaggio  | JavaScript                                                                                                       |
| Stars       | 435                                                                                                              |
| Forks       | 75                                                                                                               |
| Watchers    | 34                                                                                                               |
| Open Issues | 64                                                                                                               |
| Creato      | 2020-11-02 (5 anni fa)                                                                                           |
| Archivio    | No                                                                                                               |
| Fork        | No                                                                                                               |
| Topics      | binance-api, bitcoin, cryptocurrency-exchanges, financial-data, google-spreadsheets, trade                       |
| npm         | [https://www.npmjs.com/package/binance-to-google-sheets](https://www.npmjs.com/package/binance-to-google-sheets) |
| DeepWiki    | [deepwiki.com/diegomanuel/binance-to-google-sheets](https://deepwiki.com/diegomanuel/binance-to-google-sheets)   |

---

## 3. Attività di Sviluppo

| Metrica            | Valore              |
| ------------------ | ------------------- |
| Ultimo commit      | 2024-02-17          |
| Commit (30 giorni) | 0                   |
| Commit (90 giorni) | 0                   |
| Ultima release     | v0.6.0 (2024-02-17) |

---

## 4. Contribuenti

Totale contributors: **2** (2 umani, 0 bot)

**Bus Factor**: 🔴 1 — contributor con >10% dei commit totali

| #   | Contributor  | Contribuzioni | %     | Tipo |
| --- | ------------ | ------------- | ----- | ---- |
| 1   | @diegomanuel | 139           | 99.3% | User |
| 2   | @fabiob      | 1             | 0.7%  | User |

---

## 5. Release

| Metrica             | Valore     |
| ------------------- | ---------- |
| Totale release      | 10         |
| Ultima release      | v0.6.0     |
| Data ultima release | 2024-02-17 |

---

## 8. Issues & PR

| Metrica             | Valore |
| ------------------- | ------ |
| Issue aperte        | 64     |
| Issue chiuse (90gg) | 0      |

---

## A1 — Analisi LLM

> _Generata da `pipeline analyze` — fonte: `01-analysis/llm-analysis.md`_

# LLM Analysis: diegomanuel/binance-to-google-sheets

**Data:** 2026-03-27 **Sezione:** all **Modello:** gemini-3.1-pro-preview **Data Summary:**
01-data-summary.md

---

Di seguito l'analisi tecnica del repository `diegomanuel/binance-to-google-sheets`.

> ⚠️ **Nota di Dominio**: In qualità di evaluator specializzato in ambito GIS, rilevo immediatamente
> che questo progetto **non appartiene al dominio geospaziale**. Si tratta di uno strumento
> FinTech/Data Integration (integrazione tra exchange di criptovalute e fogli di calcolo). L'analisi
> seguente applicherà pertanto i principi generali di software engineering, omettendo le valutazioni
> su standard spaziali (es. OGC), formati vettoriali/raster o proiezioni cartografiche, in quanto
> non applicabili.

---

## 1. ARCHITETTURA

### Stack Tecnologico e Pattern Inferibili

Basandosi sui metadati forniti:

- **Linguaggio principale:** JavaScript.
- **Ambiente di esecuzione:** Google Spreadsheets add-on. Questo implica quasi certamente l'utilizzo
  di **Google Apps Script (GAS)** come framework sottostante.
- **Pattern architetturale:** Integrazione API Point-to-Point. La descrizione specifica "without any
  intermediaries", suggerendo che lo script effettua chiamate REST dirette (presumibilmente tramite
  `UrlFetchApp` di GAS) verso le API pubbliche/private di Binance.

### Valutazione Scalabilità e Manutenibilità

- **Pro:** L'assenza di intermediari (server middleware) riduce la latenza, elimina i costi di
  hosting per l'utente e migliora teoricamente la privacy dei dati.
- **Contro (Inferenza tecnica):** L'architettura basata su Google Apps Script è soggetta a rigidi
  limiti di quota (es. tempo massimo di esecuzione per script, numero di chiamate URL esterne
  giornaliere). Se l'utente richiede moli di dati storici elevate, l'architettura potrebbe non
  scalare adeguatamente.

**Raccomandazioni Architetturali:**

- Verificare (se si avesse accesso al codice) l'implementazione di meccanismi di retry con
  _exponential backoff_ per gestire i rate limit delle API di Binance.

---

## 2. SICUREZZA

### Score OpenSSF e Processi

- **OpenSSF Scorecard:** `[DATO MANCANTE]`. Non sono stati forniti dati relativi alla scorecard
  OpenSSF.
- **Processi di Security:** Non emergono evidenze di processi di sicurezza automatizzati dai
  metadati forniti.

### Rischi Identificati

> ⚠️ **Rischio Critico - Gestione Credenziali:** Poiché il tool si connette alle API di Binance (che
> richiedono API Key e Secret Key per dati privati), e operando in ambiente Google Sheets, esiste un
> rischio intrinseco legato a come queste chiavi vengono memorizzate. Se salvate in chiaro nelle
> celle del foglio o non gestite tramite il `PropertiesService` crittografato di GAS, rappresentano
> una grave vulnerabilità.

> ⚠️ **Rischio di Obsolescenza:** L'ultimo commit risale al 2024-02-17. Nel contesto delle API degli
> exchange di criptovalute, che subiscono deprecazioni e aggiornamenti frequenti, un progetto
> inattivo da oltre un anno è ad alto rischio di rottura (breaking changes non gestite).

**Raccomandazioni di Sicurezza:**

- Implementare audit automatizzati (es. GitHub Actions con Dependabot o CodeQL) se il progetto
  utilizza dipendenze npm (es. tramite `clasp` per lo sviluppo GAS).
- Fornire documentazione chiara all'utente finale sui permessi richiesti dall'add-on (OAuth scopes
  di Google).

---

## 3. QUALITÀ

### Contributor e Bus Factor

Il progetto presenta una centralizzazione estrema dello sviluppo.

| Metrica                | Valore |
| :--------------------- | :----- |
| **Totale Contributor** | 2      |
| **Bus Factor**         | 1      |

**Distribuzione:** | Contributor | Contribuzioni | Percentuale | | :--- | :--- | :--- | |
@diegomanuel | 139 | 99.3% | | @fabiob | 1 | 0.7% |

- **Analisi:** Il progetto è di fatto un _one-man project_. Il Bus Factor pari a 1 rappresenta un
  rischio sistemico per la continuità del software.

### Velocity di Sviluppo e Maturità

- **Età del progetto:** Creato a Novembre 2020 (oltre 3 anni di vita), dimostra una certa longevità
  iniziale.
- **Adozione:** 435 Stars e 75 Forks indicano un'ottima validazione dell'idea e un forte interesse
  da parte della community.
- **Velocity attuale:** **Stagnante**. Con 0 commit negli ultimi 30 e 90 giorni, e l'ultima release
  (v0.6.0) ferma a Febbraio 2024, il progetto è attualmente dormiente.

### Gestione Issue e PR

- **Open Issues:** 64
- **Analisi:** Il rapporto tra issue aperte (64) e l'assenza di attività recente è un indicatore
  negativo. Suggerisce un accumulo di debito tecnico, bug non risolti o feature request ignorate.
  Per un progetto con 435 stars, 64 issue aperte senza manutenzione attiva indicano che il
  maintainer non riesce più a supportare la base utenti.

**Raccomandazioni per la Qualità:**

- **Per il maintainer:** Considerare l'aggiunta di un avviso nel `README.md` che dichiari lo stato
  attuale del progetto (es. "Looking for maintainers" o "Archived/Dormant") per gestire le
  aspettative degli utenti.
- **Per la community:** Dato l'alto numero di fork (75), esplorare la rete dei fork per identificare
  se un altro sviluppatore ha preso in carico la manutenzione attiva del codice creando un fork
  principale alternativo.

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
