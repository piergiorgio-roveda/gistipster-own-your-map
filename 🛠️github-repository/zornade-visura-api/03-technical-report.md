---
repo: zornade/visura-api
url: https://github.com/zornade/visura-api
date_analysis: 2026-03-26
version: 1
analyst: pipeline/report-builder
status: draft
---

# zornade/visura-api — Valutazione Tecnica

> **Repository**: [zornade/visura-api](https://github.com/zornade/visura-api) | **Data analisi**:
> 2026-03-26 | **Versione**: 1

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

| Indicatore | Status    | Note                                                    |
| ---------- | --------- | ------------------------------------------------------- |
| Salute     | 🟡 6.7/10 | score composito (attività + BF + issue + release + sec) |
| Attività   | 🟢 Attivo | ultimo commit: 2026-03-20                               |
| Bus Factor | 🟡 2      | contributor dominanti                                   |
| Sicurezza  | ⚪ N/D    | OpenSSF Scorecard                                       |
| CI/CD      | ⚪ N/D    | da topics repo                                          |
| Community  | 🟡 618    | ★ stars                                                 |

---

## 1. Informazioni Generali

| Campo       | Valore                                                                     |
| ----------- | -------------------------------------------------------------------------- |
| Repository  | [zornade/visura-api](https://github.com/zornade/visura-api)                |
| Categoria   | Backend                                                                    |
| Licenza     | AGPL-3.0                                                                   |
| Linguaggio  | Python                                                                     |
| Stars       | 618                                                                        |
| Forks       | 71                                                                         |
| Watchers    | 13                                                                         |
| Open Issues | 2                                                                          |
| Creato      | 2026-03-03 (1 mese fa)                                                     |
| Archivio    | No                                                                         |
| Fork        | No                                                                         |
| Homepage    | https://zornade.com/api-particelle-catastali                               |
| PyPI        | [https://pypi.org/project/visura-api](https://pypi.org/project/visura-api) |
| DeepWiki    | [deepwiki.com/zornade/visura-api](https://deepwiki.com/zornade/visura-api) |

---

## 3. Attività di Sviluppo

| Metrica            | Valore              |
| ------------------ | ------------------- |
| Ultimo commit      | 2026-03-20          |
| Commit (30 giorni) | 10                  |
| Commit (90 giorni) | 10                  |
| Trend commit       | ↑ In crescita       |
| Ultima release     | v0.1.0 (2026-03-13) |

---

## 4. Contribuenti

Totale contributors: **2** (2 umani, 0 bot)

**Bus Factor**: 🟡 2 — contributor con >10% dei commit totali

| #   | Contributor | Contribuzioni | %     | Tipo |
| --- | ----------- | ------------- | ----- | ---- |
| 1   | @zornade    | 4             | 80.0% | User |
| 2   | @alestucci  | 1             | 20.0% | User |

---

## 5. Release

| Metrica             | Valore     |
| ------------------- | ---------- |
| Totale release      | 1          |
| Ultima release      | v0.1.0     |
| Data ultima release | 2026-03-13 |

---

## 8. Issues & PR

| Metrica             | Valore |
| ------------------- | ------ |
| Issue aperte        | 2      |
| Issue chiuse (90gg) | 0      |

---

## A1 — Analisi LLM

> _Generata da `pipeline analyze` — fonte: `01-analysis/llm-analysis.md`_

# LLM Analysis: zornade/visura-api

**Data:** 2026-03-26 **Sezione:** all **Modello:** gemini-3.1-pro-preview **Data Summary:**
01-data-summary.md

---

Ecco l'analisi tecnica del repository `zornade/visura-api`, condotta in base ai metadati forniti.

---

# Analisi Repository: `zornade/visura-api`

**Contesto di Dominio:** Il progetto si colloca in un'area critica per il GIS in Italia:
l'acquisizione di dati catastali. Il portale SISTER (Agenzia delle Entrate) è la fonte primaria per
questi dati, fondamentali per analisi spaziali, urbanistica e real estate. L'assenza di API moderne
ufficiali rende strumenti di "estrazione automatizzata" altamente richiesti dalla community
geospaziale.

## 1. ARCHITETTURA

Essendo un progetto di recentissima creazione (23 giorni al momento della rilevazione),
l'architettura è presumibilmente in fase embrionale.

- **Stack Tecnologico:** Python. Scelta standard e ottimale per il dominio GIS e per task di
  automazione/scraping. [DATO MANCANTE] Non sono specificati i framework utilizzati (es.
  FastAPI/Flask per l'API, o Selenium/Playwright/BeautifulSoup per l'estrazione).
- **Pattern Architetturali Inferibili:** Il termine "estrazione automatizzata" associato a un
  portale legacy (SISTER) indica un pattern di tipo _Web Scraping_ o _RPA (Robotic Process
  Automation)_ esposto tramite un layer API (Facade pattern).
- **Manutenibilità e Scalabilità:**
  - _Fragilità intrinseca:_ Qualsiasi architettura basata su scraping di portali di terze parti è
    intrinsecamente fragile. Modifiche alla UI o ai sistemi di autenticazione di SISTER causeranno
    la rottura (breaking) dell'API.
  - _Interoperabilità GIS:_ [DATO MANCANTE] Non è noto se l'API restituisca i dati in formati
    standard GIS (es. GeoJSON per le geometrie catastali, se estratte) o in JSON generico.

> ⚠️ **FINDING CRITICO (Architettura):** L'accoppiamento forte con l'interfaccia non documentata del
> portale SISTER rappresenta il rischio architetturale primario. _Raccomandazione:_ Implementare
> un'architettura a strati con adapter specifici per il parsing, isolando la logica di estrazione da
> quella di esposizione API per facilitare rapidi fix quando il portale sorgente cambia.

## 2. SICUREZZA

- **OpenSSF Scorecard:** [DATO MANCANTE] Nessun dato disponibile sui controlli di sicurezza
  automatizzati.
- **Processi di Security:** [DATO MANCANTE] Non vi è evidenza di policy di sicurezza (es.
  `SECURITY.md`).
- **Rischi Identificati:**
  1.  **Gestione Credenziali:** L'accesso a SISTER richiede credenziali nominali e spesso sistemi di
      ricarica del castelletto. L'API deve gestire questi segreti in modo estremamente sicuro,
      evitando log in chiaro.
  2.  **Rischio Legale/Compliance:** L'estrazione automatizzata (scraping) da portali governativi
      può violare i Termini di Servizio (ToS).
  3.  **Licenza AGPL-3.0:** Sebbene sia una scelta legittima, la licenza AGPL-3.0 è fortemente
      virale (copyleft). Qualsiasi servizio backend che integri questa API via rete potrebbe essere
      costretto a rilasciare il proprio codice sorgente. Questo è un "rischio di compliance" per
      l'adozione in ambito enterprise.

> ⚠️ **FINDING CRITICO (Sicurezza/Compliance):** L'uso della licenza AGPL-3.0 per un'API di
> estrazione dati limiterà severamente l'adozione commerciale/enterprise del tool.
> _Raccomandazione:_ Aggiungere documentazione chiara su come gestire le credenziali SISTER in modo
> sicuro (es. via variabili d'ambiente) e chiarire le implicazioni della licenza AGPL per gli
> utilizzatori.

## 3. QUALITÀ

Il dato più rilevante di questa analisi è la **trazione anomala e straordinaria** del progetto in
rapporto alla sua età.

### Metriche di Adozione e Sviluppo

| Metrica          | Valore    | Analisi                                                                                                                                          |
| :--------------- | :-------- | :----------------------------------------------------------------------------------------------------------------------------------------------- |
| **Età progetto** | 23 giorni | Progetto neonato (creato 03-03-2026).                                                                                                            |
| **Stars**        | 618       | **Eccezionale.** Ottenere >600 star in 3 settimane indica che il progetto risolve un _pain point_ massivo nella community GIS/PropTech italiana. |
| **Forks**        | 71        | Ottimo tasso di conversione Star/Fork (~11%), indica reale intenzione di utilizzo o contribuzione.                                               |
| **Maturità**     | v0.1.0    | Rilascio Alpha/Beta. Il software non è da considerarsi production-ready.                                                                         |

### Contributor e Bus Factor

- **Bus Factor:** 2 (di fatto 1).
- Il creatore `@zornade` detiene l'80% delle contribuzioni tracciate nella top list. Il progetto è
  un tipico _single-maintainer project_ nelle sue fasi iniziali.
- _Nota sui dati:_ Si rileva una discrepanza nei metadati (10 commit totali negli ultimi 30gg, ma la
  tabella contributor ne somma 5). Si assume che la tabella mostri solo i top contributor o che
  alcuni commit non siano associati ad account GitHub validi.

### Gestione Issue

- **Open Issues:** 2. Un numero fisiologico e gestibile, coerente con un progetto appena rilasciato
  (v0.1.0 il 13-03-2026).

> ⚠️ **FINDING CRITICO (Qualità):** Il progetto ha generato un hype enorme (618 stars) ma poggia
> sulle spalle di un singolo sviluppatore principale (Bus Factor critico) ed è in versione 0.1.0.
> _Raccomandazione:_ Il maintainer deve capitalizzare immediatamente sull'interesse della community
> (71 fork) delegando task, definendo linee guida per la contribuzione (`CONTRIBUTING.md`) e
> promuovendo altri sviluppatori a maintainer per mitigare il rischio di abbandono (burnout).

---

## Sintesi della Valutazione

`zornade/visura-api` è un progetto ad **altissimo potenziale** che colma una lacuna storica
nell'infrastruttura dati GIS italiana (l'accesso programmatico al catasto). Tuttavia, si tratta di
un _Proof of Concept_ avanzato (v0.1.0) con elevati rischi architetturali (dipendenza da scraping) e
di compliance (AGPL-3.0). L'adozione in ambienti di produzione GIS aziendali è attualmente
sconsigliata fino al raggiungimento di una maggiore maturità (v1.0.0) e all'ampliamento del team di
maintainer.

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
