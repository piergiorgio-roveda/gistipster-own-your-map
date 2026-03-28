---
repo: postgis/postgis
url: https://github.com/postgis/postgis
date_analysis: 2026-03-26
version: 1
analyst: pipeline/report-builder
status: draft
---

# postgis/postgis — Valutazione Tecnica

> **Repository**: [postgis/postgis](https://github.com/postgis/postgis) | **Data analisi**:
> 2026-03-26 | **Versione**: 1

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

| Indicatore | Status    | Note                                                    |
| ---------- | --------- | ------------------------------------------------------- |
| Salute     | 🟡 5.6/10 | score composito (attività + BF + issue + release + sec) |
| Attività   | 🟢 Attivo | ultimo commit: 2026-03-25                               |
| Bus Factor | 🟢 3      | contributor dominanti                                   |
| Sicurezza  | ⚪ N/D    | OpenSSF Scorecard                                       |
| CI/CD      | ⚪ N/D    | da topics repo                                          |
| Community  | 🟡 2067   | ★ stars                                                 |

---

## 1. Informazioni Generali

| Campo       | Valore                                                               |
| ----------- | -------------------------------------------------------------------- |
| Repository  | [postgis/postgis](https://github.com/postgis/postgis)                |
| Licenza     | GPL-2.0                                                              |
| Linguaggio  | PLpgSQL                                                              |
| Stars       | 2067                                                                 |
| Forks       | 422                                                                  |
| Watchers    | 66                                                                   |
| Open Issues | 3                                                                    |
| Creato      | 2012-05-22 (13 anni fa)                                              |
| Archivio    | No                                                                   |
| Fork        | No                                                                   |
| Topics      | c, geospatial, gis, plpgsql, postgis, postgresql                     |
| Homepage    | https://postgis.net                                                  |
| DeepWiki    | [deepwiki.com/postgis/postgis](https://deepwiki.com/postgis/postgis) |

---

## 3. Attività di Sviluppo

| Metrica            | Valore        |
| ------------------ | ------------- |
| Ultimo commit      | 2026-03-25    |
| Commit (30 giorni) | 10            |
| Commit (90 giorni) | 10            |
| Trend commit       | ↑ In crescita |

---

## 4. Contribuenti

Totale contributors: **30** (30 umani, 0 bot)

**Bus Factor**: 🟢 3 — contributor con >10% dei commit totali

| #   | Contributor    | Contribuzioni | %     | Tipo |
| --- | -------------- | ------------- | ----- | ---- |
| 1   | @strk          | 6198          | 36.8% | User |
| 2   | @robe2         | 4471          | 26.5% | User |
| 3   | @pramsey       | 2915          | 17.3% | User |
| 4   | @dustymugs     | 831           | 4.9%  | User |
| 5   | @yellow-affrc  | 442           | 2.6%  | User |
| 6   | @Komzpa        | 330           | 2.0%  | User |
| 7   | @dr-jts        | 220           | 1.3%  | User |
| 8   | @markusschaber | 150           | 0.9%  | User |
| 9   | @davidblasby   | 138           | 0.8%  | User |
| 10  | @Algunenano    | 137           | 0.8%  | User |
| 11  | @weblate       | 133           | 0.8%  | User |
| 12  | @dbaston       | 121           | 0.7%  | User |

_... e altri 18 contributors_

---

## 8. Issues & PR

| Metrica             | Valore |
| ------------------- | ------ |
| Issue aperte        | 3      |
| Issue chiuse (90gg) | 0      |

---

## A1 — Analisi LLM

> _Generata da `pipeline analyze` — fonte: `01-analysis/llm-analysis.md`_

# LLM Analysis: postgis/postgis

**Data:** 2026-03-26 **Sezione:** all **Modello:** gemini-3.1-pro-preview **Data Summary:**
01-data-summary.md

---

Ecco l'analisi tecnica del repository `postgis/postgis` basata esclusivamente sui metadati forniti.

> ⚠️ **FINDING CRITICO PRELIMINARE**: La descrizione del repository indica esplicitamente che si
> tratta di un **[mirror]**. Questo dettaglio è fondamentale poiché altera l'interpretazione di
> metriche standard come la gestione delle Issue e le dinamiche di contribuzione su GitHub. Il vero
> ciclo di vita dello sviluppo (SDLC) avviene verosimilmente su un'infrastruttura upstream (es.
> OSGeo Git/SVN o Trac).

---

## 1. ARCHITETTURA

### Stack Tecnologico e Pattern

- **Linguaggio Principale**: Il linguaggio rilevato è **PLpgSQL**. Questo conferma la natura del
  progetto come estensione nativa per database relazionali, progettata per eseguire logica
  geospaziale direttamente all'interno del motore di database.
- **Pattern Architetturale**: _Database Extension_. Il progetto estende le capacità di PostgreSQL
  aggiungendo tipi di dati spaziali (geometrie/geografie), indici spaziali e funzioni analitiche.
- **Licenza**: **GPL-2.0**. Una licenza copyleft forte. Questo impone vincoli architetturali severi
  per i software downstream che intendono distribuire o linkare direttamente l'estensione,
  richiedendo la compatibilità della licenza.

### Manutenibilità e Scalabilità

- **Longevità**: Creato nel maggio 2012 (circa 14 anni di vita rispetto alla data di analisi).
  Questo indica un'architettura estremamente matura e consolidata nel tempo.
- **Adozione**: Con 2067 Stars e 422 Forks, il progetto dimostra un'altissima validazione da parte
  della community GIS, suggerendo che l'architettura è scalabile e risponde efficacemente ai
  requisiti di produzione.

---

## 2. SICUREZZA

### Metriche e Processi

- **OpenSSF Scorecard**: [DATO MANCANTE]. Non sono forniti dati relativi allo score OpenSSF.
- **Processi di Security**: Essendo un mirror, è altamente probabile che i controlli di sicurezza
  automatizzati (es. Dependabot, CodeQL) non siano configurati o visibili su questo repository
  GitHub, ma siano gestiti nel repository sorgente.

### Rischi Identificati

> ⚠️ **RISCHIO DI CONCENTRAZIONE (Key Person Risk)**: Il rischio di sicurezza/continuità più
> evidente dai dati è legato al fattore umano. Tre soli sviluppatori controllano oltre l'80% della
> codebase storica. La perdita di uno di questi nodi comporterebbe un grave rischio per la
> manutenzione di componenti critici.

- **Raccomandazione**: Verificare le policy di sicurezza, la gestione delle vulnerabilità (CVE) e i
  controlli di supply chain direttamente sull'infrastruttura upstream ufficiale, non basandosi su
  questo mirror.

---

## 3. QUALITÀ

### Distribuzione Contributor e Bus Factor

Il repository conta 30 contributor umani totali, ma la distribuzione del lavoro è fortemente
asimmetrica:

| Fascia Contributiva       | Contributor                        | % Totale Commit (Storico) |
| :------------------------ | :--------------------------------- | :------------------------ |
| **Core (Top 3)**          | @strk, @robe2, @pramsey            | **80.6%**                 |
| **Maintainers (Top 4-6)** | @dustymugs, @yellow-affrc, @Komzpa | **9.5%**                  |
| **Occasionali/Altri**     | 24 contributors                    | **~9.9%**                 |

- **Bus Factor = 3**: Questo è un valore basso per un progetto di tale importanza globale. Indica
  che la conoscenza profonda del dominio GIS e del codice è centralizzata. Tuttavia, è un pattern
  comune in progetti open source di nicchia altamente specializzati (matematica spaziale, geodesia).
- **Internazionalizzazione**: La presenza di `@weblate` (133 commit) indica un processo
  automatizzato e attivo per la traduzione e localizzazione (i18n) del software, segno di alta
  qualità e attenzione all'utenza globale.

### Velocity e Gestione Issue

- **Velocity Recente**: Sono stati registrati 10 commit negli ultimi 30 giorni e 10 negli ultimi 90
  giorni.
  - _Inferenza_: Tutta l'attività dell'ultimo trimestre si è concentrata nell'ultimo mese. Questo
    andamento "a scatti" è tipico dei repository mirror che vengono sincronizzati periodicamente
    tramite batch o in prossimità di nuove release. L'ultimo commit risale al giorno precedente
    l'estrazione dei dati (2026-03-25), confermando che il progetto è vivo.
- **Gestione Issue**: Solo **3 Open Issues**.
  - _Inferenza_: In un progetto con oltre 2000 star e 14 anni di storia, 3 issue aperte sono
    un'anomalia statistica. Questo conferma in modo inequivocabile che GitHub _non_ è l'issue
    tracker ufficiale del progetto. Gli utenti vengono probabilmente reindirizzati altrove per il
    bug reporting.

---

## SINTESI E RACCOMANDAZIONI AZIONABILI

1.  **Per gli Sviluppatori/Integratori Downstream**:
    - _Azione_: Non utilizzare GitHub per segnalare bug o proporre Pull Request senza prima aver
      consultato le linee guida di contribuzione (CONTRIBUTING.md), poiché questo è solo un mirror.
      Cercare la vera repository upstream.
    - _Azione_: Valutare attentamente l'impatto della licenza GPL-2.0 sulla propria architettura
      software prima dell'integrazione.

2.  **Per i Maintainer (Valutazione della Governance)**:
    - _Azione_: Il Bus Factor di 3 rappresenta un debito organizzativo. È raccomandabile avviare
      programmi di mentorship o incentivare i contributor di fascia media (es. @dustymugs,
      @yellow-affrc) ad assumere maggiore ownership su moduli specifici per mitigare il rischio di
      abbandono dei top contributor storici.
    - _Azione_: Se non già presente, aggiungere un avviso molto visibile nel `README.md` su GitHub
      che disabiliti le Issue o reindirizzi chiaramente gli utenti al tracker ufficiale, per evitare
      frammentazione delle segnalazioni.

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
