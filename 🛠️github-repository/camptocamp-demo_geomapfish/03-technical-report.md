---
repo: camptocamp/demo_geomapfish
url: https://github.com/camptocamp/demo_geomapfish
date_analysis: 2026-03-26
version: 1
analyst: pipeline/report-builder
status: draft
---

# camptocamp/demo_geomapfish — Valutazione Tecnica

> **Repository**: [camptocamp/demo_geomapfish](https://github.com/camptocamp/demo_geomapfish) |
> **Data analisi**: 2026-03-26 | **Versione**: 1

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
| Salute     | 🟡 4.4/10 | score composito (attività + BF + issue + release + sec) |
| Attività   | 🟢 Attivo | ultimo commit: 2026-03-26                               |
| Bus Factor | 🟡 2      | contributor dominanti                                   |
| Sicurezza  | ⚪ N/D    | OpenSSF Scorecard                                       |
| CI/CD      | ⚪ N/D    | da topics repo                                          |
| Community  | ⚪ 7      | ★ stars                                                 |

---

## 1. Informazioni Generali

| Campo       | Valore                                                                                     |
| ----------- | ------------------------------------------------------------------------------------------ |
| Repository  | [camptocamp/demo_geomapfish](https://github.com/camptocamp/demo_geomapfish)                |
| Licenza     | BSD-2-Clause                                                                               |
| Linguaggio  | PLpgSQL                                                                                    |
| Stars       | 7                                                                                          |
| Forks       | 15                                                                                         |
| Watchers    | 14                                                                                         |
| Open Issues | 7                                                                                          |
| Creato      | 2012-09-28 (13 anni fa)                                                                    |
| Archivio    | No                                                                                         |
| Fork        | No                                                                                         |
| Topics      | geomapfish, geospatial                                                                     |
| DeepWiki    | [deepwiki.com/camptocamp/demo_geomapfish](https://deepwiki.com/camptocamp/demo_geomapfish) |

---

## 3. Attività di Sviluppo

| Metrica            | Valore        |
| ------------------ | ------------- |
| Ultimo commit      | 2026-03-26    |
| Commit (30 giorni) | 10            |
| Commit (90 giorni) | 10            |
| Trend commit       | ↑ In crescita |

---

## 4. Contribuenti

Totale contributors: **25** (20 umani, 5 bot)

**Bus Factor**: 🟡 2 — contributor con >10% dei commit totali

| #   | Contributor     | Contribuzioni | %     | Tipo |
| --- | --------------- | ------------- | ----- | ---- |
| 1   | @sbrunner       | 2124          | 69.8% | User |
| 2   | @ger-benjamin   | 74            | 2.4%  | User |
| 3   | @fredj          | 35            | 1.2%  | User |
| 4   | @yjacolin       | 35            | 1.2%  | User |
| 5   | @arnaud-morvan  | 31            | 1.0%  | User |
| 6   | @c2c-bot-gis-ci | 24            | 0.8%  | User |
| 7   | @marionb        | 17            | 0.6%  | User |
| 8   | @julsbreakdown  | 12            | 0.4%  | User |
| 9   | @llienher       | 11            | 0.4%  | User |
| 10  | @ochriste       | 9             | 0.3%  | User |
| 11  | @pvalsecc       | 9             | 0.3%  | User |
| 12  | @ybolognini     | 7             | 0.2%  | User |

_... e altri 8 contributors_

---

## 8. Issues & PR

| Metrica             | Valore |
| ------------------- | ------ |
| Issue aperte        | 7      |
| Issue chiuse (90gg) | 0      |

---

## A1 — Analisi LLM

> _Generata da `pipeline analyze` — fonte: `01-analysis/llm-analysis.md`_

# LLM Analysis: camptocamp/demo_geomapfish

**Data:** 2026-03-26 **Sezione:** all **Modello:** gemini-3.1-pro-preview **Data Summary:**
01-data-summary.md

---

Ecco l'analisi tecnica del repository `camptocamp/demo_geomapfish` basata esclusivamente sui
metadati forniti.

---

## Sintesi del Progetto

Il repository appare come un progetto di dimostrazione o template (deducibile dal prefisso `demo_`)
per l'ecosistema **GeoMapFish**, mantenuto dall'organizzazione Camptocamp. Con oltre 13 anni di vita
(creato nel 2012), rappresenta un progetto maturo, ma le metriche di popolarità (7 stars, 15 forks)
indicano che è utilizzato principalmente come strumento di utilità interna o come base di partenza
(template) per implementazioni specifiche, piuttosto che come libreria o framework community-driven.

---

## 1. ARCHITETTURA

### Stack Tecnologico e Pattern

- **Linguaggio Principale:** L'identificazione di **PLpgSQL** come linguaggio primario è un
  indicatore architetturale forte in ambito GIS. Suggerisce che il repository contenga logica di
  business geospaziale fortemente accoppiata al database (presumibilmente PostgreSQL con estensione
  PostGIS). Questo pattern ("Thick Database") è comune in applicazioni GIS legacy o ad alte
  prestazioni dove le operazioni spaziali vengono delegate direttamente al motore DB per minimizzare
  il trasferimento dati.
- **Automazione:** La presenza del contributor `@c2c-bot-gis-ci` conferma l'esistenza di una
  pipeline di Continuous Integration (CI) specifica per il dominio GIS.

### Valutazione Manutenibilità e Scalabilità

- **Pro:** L'uso di PLpgSQL per le operazioni spaziali garantisce ottime performance
  nell'elaborazione di geometrie complesse. La presenza di un bot di CI indica che i processi di
  build/test sono automatizzati, migliorando la manutenibilità.
- **Contro:** Una forte dipendenza da PLpgSQL può rendere il refactoring complesso e limitare la
  portabilità verso altri RDBMS (sebbene in ambito GIS open source, PostGIS sia lo standard de
  facto).

**Raccomandazioni:**

- Verificare che la logica PLpgSQL sia adeguatamente coperta da test automatizzati all'interno della
  pipeline CI, dato che il testing del codice database è storicamente più complesso rispetto al
  codice applicativo.

---

## 2. SICUREZZA

### Metriche e Processi

- **OpenSSF Scorecard:** `[DATO MANCANTE]` - Non sono stati forniti dati relativi allo score
  OpenSSF, rendendo impossibile una valutazione quantitativa delle best practice di sicurezza (es.
  branch protection, token permissions).
- **Licenza:** Il progetto utilizza una licenza **BSD-2-Clause**. Si tratta di una licenza
  permissiva che non pone vincoli virali (copyleft), rendendo il codice sicuro per l'inclusione in
  contesti enterprise o proprietari.

### Rischi Identificati

> ⚠️ **RISCHIO CRITICO - Continuità Operativa (Key Person Risk):** Il rischio di sicurezza
> principale identificato non deriva dal codice, ma dalla gestione del progetto. Un _Bus Factor_
> pari a 2 rappresenta una vulnerabilità critica per la supply chain di chiunque dipenda da questo
> repository.

**Raccomandazioni:**

- Implementare l'analisi OpenSSF Scorecard per ottenere visibilità oggettiva sulle pratiche di
  sicurezza del repository.
- Assicurarsi che i permessi di merge e le chiavi crittografiche/segreti utilizzati dal bot
  `@c2c-bot-gis-ci` siano ruotati regolarmente e non dipendano dall'account del main contributor.

---

## 3. QUALITÀ

### Distribuzione Contributor e Bus Factor

La distribuzione dei contributi è gravemente sbilanciata: | Contributor | Commits | Percentuale |
Ruolo Inferito | | :--- | :--- | :--- | :--- | | `@sbrunner` | 2124 | 69.8% | Lead Maintainer / BDFL
| | `@ger-benjamin` | 74 | 2.4% | Contributor occasionale | | _Altri 23_ | < 35 cad. | < 2% cad. |
Drive-by contributors / Bot |

Il progetto è di fatto mantenuto da una singola persona (`@sbrunner`), con un divario enorme
rispetto al secondo contributor. Questo indica una scarsa condivisione della conoscenza (knowledge
silo) all'interno del team.

### Velocity di Sviluppo e Gestione Issue

- **Andamento Commit:** I dati mostrano 10 commit negli ultimi 30 giorni e 10 commit negli ultimi 90
  giorni. Questo significa che il progetto è stato completamente inattivo per 60 giorni, per poi
  avere un picco di attività recente. Questo pattern "a scatti" è tipico dei repository di
  demo/template, che vengono aggiornati in batch solo in concomitanza con le release del framework
  principale (GeoMapFish).
- **Gestione Issue:** Ci sono 7 issue aperte. A fronte di un progetto di 13 anni, un numero così
  basso suggerisce due ipotesi: o il repository è estremamente stabile, oppure le issue vengono
  tracciate altrove (es. nel repository principale del framework).

### Maturità del Progetto

Il rapporto tra Stars (7) e Forks (15) è atipico per un progetto standard, ma perfettamente coerente
con un repository "demo". Gli utenti non "apprezzano" (star) il progetto, ma lo "copiano" (fork) per
usarlo come boilerplate per le proprie infrastrutture WebGIS.

**Raccomandazioni:**

- **Mitigazione Bus Factor:** È imperativo avviare un processo di shadow-mentoring. Almeno un altro
  sviluppatore dell'organizzazione Camptocamp dovrebbe essere affiancato a `@sbrunner` per
  bilanciare le code review e la gestione delle release.
- **Documentazione:** Dato l'alto numero di fork rispetto all'utenza attiva, assicurarsi che il
  `README.md` e la documentazione di setup siano estremamente dettagliati, per ridurre il carico di
  supporto sul singolo maintainer.

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
