---
repo: kartaview/upload-scripts
url: https://github.com/kartaview/upload-scripts
date_analysis: 2026-03-27
version: 1
analyst: pipeline/report-builder
status: draft
---

# kartaview/upload-scripts — Valutazione Tecnica

> **Repository**: [kartaview/upload-scripts](https://github.com/kartaview/upload-scripts) | **Data
> analisi**: 2026-03-27 | **Versione**: 1

---

## Indice

| #   | Sezione               | Disponibilità    |
| --- | --------------------- | ---------------- |
| 1   | Quick Summary         | obbligatoria     |
| 2   | Informazioni Generali | obbligatoria     |
| 3   | Attività di Sviluppo  | dati disponibili |
| 4   | Contribuenti          | dati disponibili |
| 8   | Issues & PR           | dati disponibili |
| A1  | Analisi LLM           | allegato         |

---

## Quick Summary

| Indicatore | Status        | Note                                                    |
| ---------- | ------------- | ------------------------------------------------------- |
| Salute     | 🔴 2.2/10     | score composito (attività + BF + issue + release + sec) |
| Attività   | 🟡 Rallentato | ultimo commit: 2025-04-03                               |
| Bus Factor | 🟡 2          | contributor dominanti                                   |
| Sicurezza  | ⚪ N/D        | OpenSSF Scorecard                                       |
| CI/CD      | ⚪ N/D        | da topics repo                                          |
| Community  | ⚪ 64         | ★ stars                                                 |

---

## 1. Informazioni Generali

| Campo       | Valore                                                                                 |
| ----------- | -------------------------------------------------------------------------------------- |
| Repository  | [kartaview/upload-scripts](https://github.com/kartaview/upload-scripts)                |
| Categoria   | Backend                                                                                |
| Licenza     | MIT                                                                                    |
| Linguaggio  | Python                                                                                 |
| Stars       | 64                                                                                     |
| Forks       | 32                                                                                     |
| Watchers    | 16                                                                                     |
| Open Issues | 27                                                                                     |
| Creato      | 2016-07-20 (9 anni fa)                                                                 |
| Archivio    | No                                                                                     |
| Fork        | No                                                                                     |
| DeepWiki    | [deepwiki.com/kartaview/upload-scripts](https://deepwiki.com/kartaview/upload-scripts) |

---

## 3. Attività di Sviluppo

| Metrica            | Valore     |
| ------------------ | ---------- |
| Ultimo commit      | 2025-04-03 |
| Commit (30 giorni) | 0          |
| Commit (90 giorni) | 0          |

---

## 4. Contribuenti

Totale contributors: **8** (8 umani, 0 bot)

**Bus Factor**: 🟡 2 — contributor con >10% dei commit totali

| #   | Contributor       | Contribuzioni | %     | Tipo |
| --- | ----------------- | ------------- | ----- | ---- |
| 1   | @salabogdan       | 25            | 53.2% | User |
| 2   | @alrs             | 13            | 27.7% | User |
| 3   | @chip-grab        | 3             | 6.4%  | User |
| 4   | @ciprianh-telenav | 2             | 4.3%  | User |
| 5   | @mfa              | 1             | 2.1%  | User |
| 6   | @karcsesz         | 1             | 2.1%  | User |
| 7   | @joshinils        | 1             | 2.1%  | User |
| 8   | @kudarisenmon     | 1             | 2.1%  | User |

---

## 8. Issues & PR

| Metrica             | Valore |
| ------------------- | ------ |
| Issue aperte        | 27     |
| Issue chiuse (90gg) | 0      |

---

## A1 — Analisi LLM

> _Generata da `pipeline analyze` — fonte: `01-analysis/llm-analysis.md`_

# LLM Analysis: kartaview/upload-scripts

**Data:** 2026-03-27 **Sezione:** all **Modello:** gemini-3.1-pro-preview **Data Summary:**
01-data-summary.md

---

Ecco l'analisi tecnica del repository **kartaview/upload-scripts**, basata esclusivamente sui
metadati forniti.

---

## Sintesi del Progetto

Il repository ospita script in **Python** dedicati all'upload di dati (presumibilmente immagini
georeferenziate e tracce GPS) verso la piattaforma GIS KartaView. Creato nel 2016, il progetto ha
raggiunto una fase di maturità avanzata, ma i dati attuali indicano uno stato di forte inattività o
potenziale abbandono.

---

## 1. ARCHITETTURA

### Stack Tecnologico e Pattern Inferibili

- **Linguaggio Principale:** Python.
- **Dominio:** GIS / Data Ingestion. Trattandosi di "upload-scripts" per KartaView, l'architettura è
  presumibilmente composta da tool a riga di comando (CLI) o script batch progettati per gestire I/O
  di file locali (immagini, metadati spaziali), interazioni di rete (chiamate API REST verso i
  server KartaView) e gestione dell'autenticazione.
- **Licenza:** MIT (permissiva, ottima per l'integrazione in pipeline di elaborazione dati di terze
  parti).

### Valutazione Scalabilità e Manutenibilità

- **Manutenibilità:** Il progetto ha quasi 10 anni (creato a luglio 2016). I progetti Python di
  questa età, se non costantemente aggiornati, tendono a soffrire di "bit rot" (es. transizioni da
  vecchie versioni di Python, dipendenze deprecate).
- **Dati Mancanti:** [DATO MANCANTE] Non sono forniti dati su framework di test, CI/CD (es. GitHub
  Actions) o tool di linting/formatting, che sono metriche fondamentali per valutare l'effettiva
  manutenibilità del codice sorgente.

> ⚠️ **Finding Critico:** L'assenza totale di commit negli ultimi 90 giorni e l'ultimo aggiornamento
> risalente ad aprile 2025 (circa 11 mesi prima della data di report) suggeriscono che
> l'architettura non stia ricevendo aggiornamenti per supportare nuove versioni di Python o
> modifiche alle API di KartaView.

**Raccomandazioni:**

- Verificare la compatibilità degli script con le versioni di Python attualmente supportate (Python
  3.10+).
- Implementare (se assente) un file `requirements.txt` o `pyproject.toml` rigoroso per bloccare le
  versioni delle dipendenze ed evitare rotture improvvise.

---

## 2. SICUREZZA

### Score OpenSSF e Processi

- **OpenSSF Scorecard:** [DATO MANCANTE] Il punteggio non è disponibile nei metadati forniti.
- **Processi di Security:** [DATO MANCANTE] Non ci sono evidenze di policy di sicurezza
  (`SECURITY.md`), audit o flussi di vulnerability management.

### Rischi Identificati

1.  **Gestione delle Credenziali:** Gli script di upload richiedono intrinsecamente l'uso di token
    API o credenziali utente. Senza un'analisi del codice, sussiste il rischio teorico di hardcoding
    o di log in chiaro dei token.
2.  **Dipendenze Vulnerabili (Supply Chain):** Dato il blocco dello sviluppo (0 commit in 90+
    giorni), è altamente probabile che le librerie di terze parti utilizzate (es. librerie per
    richieste HTTP come `requests`) presentino vulnerabilità note (CVE) non patchate.

> ⚠️ **Finding Critico:** Un progetto di rete (uploader) non manutenuto per quasi un anno è esposto
> a un rischio elevato di vulnerabilità nelle dipendenze di rete e crittografiche.

**Raccomandazioni:**

- Attivare **Dependabot** o strumenti simili (es. Renovate) per l'aggiornamento automatico delle
  dipendenze.
- Implementare **Secret Scanning** sul repository per prevenire il commit accidentale di token API
  KartaView.
- Aggiungere un file `SECURITY.md` per definire il processo di segnalazione delle vulnerabilità,
  anche se il progetto è in maintenance mode.

---

## 3. QUALITÀ

### Distribuzione Contributor e Bus Factor

Il progetto ha un totale di 8 contributor storici, ma la distribuzione del lavoro è fortemente
sbilanciata:

| Metrica            | Analisi                                                                                                                                                                                           |
| :----------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Bus Factor**     | **2**. Il progetto dipende quasi interamente da due sviluppatori.                                                                                                                                 |
| **Concentrazione** | `@salabogdan` (53.2%) e `@alrs` (27.7%) coprono insieme l'**80.9%** di tutti i commit.                                                                                                            |
| **Coda Lunga**     | Gli altri 6 contributor hanno apportato modifiche marginali (da 1 a 3 commit ciascuno), suggerendo contributi "drive-by" (es. fix di typo o piccoli bug) piuttosto che una vera community attiva. |

### Velocity di Sviluppo e Gestione Issue

- **Velocity:** Ferma. **0 commit** negli ultimi 30 e 90 giorni.
- **Gestione Issue:** Ci sono **27 Open Issues**. Rapportato al numero di Stars (64), il rapporto
  Issue/Star è estremamente alto (~42%). Questo indica un accumulo significativo di debito tecnico,
  bug non risolti o feature request ignorate.
- **Forks vs Stars:** Il repository ha 32 fork contro 64 stars (rapporto 1:2). Un numero così alto
  di fork rispetto alle star in un progetto inattivo suggerisce spesso che gli utenti sono costretti
  a forkare il codice per applicare fix custom necessari al loro funzionamento, poiché i maintainer
  originali non uniscono le Pull Request.

> ⚠️ **Finding Critico:** Il progetto presenta i classici sintomi di "abbandono" o "maintenance
> mode" non dichiarata: alto numero di issue aperte, zero attività recente e un Bus Factor critico
> concentrato su maintainer attualmente inattivi.

**Raccomandazioni:**

- **Triage delle Issue:** Eseguire una revisione delle 27 issue aperte. Chiudere quelle obsolete
  (stale) e categorizzare i bug critici.
- **Dichiarazione di Stato:** Se il progetto non è più attivamente sviluppato, aggiornare il
  `README.md` indicando chiaramente che è in _Maintenance Mode_ o _Archiviato_, per gestire le
  aspettative degli utenti GIS che cercano tool di upload.
- **Community Handoff:** Se KartaView necessita ancora di questi script, è necessario allocare tempo
  per un nuovo maintainer o incentivare i possessori dei 32 fork a consolidare le loro modifiche
  tramite Pull Request.

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
