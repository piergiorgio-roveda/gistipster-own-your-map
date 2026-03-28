---
repo: camptocamp/docker-qgis-server
url: https://github.com/camptocamp/docker-qgis-server
date_analysis: 2026-03-26
version: 1
analyst: pipeline/report-builder
status: draft
---

# camptocamp/docker-qgis-server — Valutazione Tecnica

> **Repository**: [camptocamp/docker-qgis-server](https://github.com/camptocamp/docker-qgis-server)
> | **Data analisi**: 2026-03-26 | **Versione**: 1

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
| Attività   | 🟢 Attivo | ultimo commit: 2026-03-11                               |
| Bus Factor | 🟢 3      | contributor dominanti                                   |
| Sicurezza  | ⚪ N/D    | OpenSSF Scorecard                                       |
| CI/CD      | ⚪ N/D    | da topics repo                                          |
| Community  | ⚪ 49     | ★ stars                                                 |

---

## 1. Informazioni Generali

| Campo       | Valore                                                                                           |
| ----------- | ------------------------------------------------------------------------------------------------ |
| Repository  | [camptocamp/docker-qgis-server](https://github.com/camptocamp/docker-qgis-server)                |
| Licenza     | GPL-2.0                                                                                          |
| Linguaggio  | Dockerfile                                                                                       |
| Stars       | 49                                                                                               |
| Forks       | 12                                                                                               |
| Watchers    | 15                                                                                               |
| Open Issues | 27                                                                                               |
| Creato      | 2016-10-12 (9 anni fa)                                                                           |
| Archivio    | No                                                                                               |
| Fork        | No                                                                                               |
| Topics      | geospatial                                                                                       |
| DeepWiki    | [deepwiki.com/camptocamp/docker-qgis-server](https://deepwiki.com/camptocamp/docker-qgis-server) |

---

## 3. Attività di Sviluppo

| Metrica            | Valore              |
| ------------------ | ------------------- |
| Ultimo commit      | 2026-03-11          |
| Commit (30 giorni) | 2                   |
| Commit (90 giorni) | 4                   |
| Trend commit       | ↑ In crescita       |
| Ultima release     | 3.44.0 (2025-06-23) |

---

## 4. Contribuenti

Totale contributors: **15** (9 umani, 6 bot)

**Bus Factor**: 🟢 3 — contributor con >10% dei commit totali

| #   | Contributor  | Contribuzioni | %     | Tipo |
| --- | ------------ | ------------- | ----- | ---- |
| 1   | @sbrunner    | 473           | 57.0% | User |
| 2   | @yjacolin    | 11            | 1.3%  | User |
| 3   | @pvalsecc    | 5             | 0.6%  | User |
| 4   | @ismailsunni | 2             | 0.2%  | User |
| 5   | @ochriste    | 2             | 0.2%  | User |
| 6   | @anderso     | 1             | 0.1%  | User |
| 7   | @danduk82    | 1             | 0.1%  | User |
| 8   | @fredj       | 1             | 0.1%  | User |
| 9   | @gberaudo    | 1             | 0.1%  | User |

---

## 5. Release

| Metrica             | Valore     |
| ------------------- | ---------- |
| Totale release      | 10         |
| Ultima release      | 3.44.0     |
| Data ultima release | 2025-06-23 |

---

## 8. Issues & PR

| Metrica             | Valore |
| ------------------- | ------ |
| Issue aperte        | 27     |
| Issue chiuse (90gg) | 0      |

---

## A1 — Analisi LLM

> _Generata da `pipeline analyze` — fonte: `01-analysis/llm-analysis.md`_

# LLM Analysis: camptocamp/docker-qgis-server

**Data:** 2026-03-26 **Sezione:** all **Modello:** gemini-3.1-pro-preview **Data Summary:**
01-data-summary.md

---

Ecco l'analisi tecnica del repository `camptocamp/docker-qgis-server` basata esclusivamente sui
metadati forniti.

---

# Analisi Repository: camptocamp/docker-qgis-server

Il repository ospita un progetto infrastrutturale (Infrastructure-as-Code) finalizzato alla
containerizzazione di **QGIS Server**, un componente critico in ambito GIS per la pubblicazione di
servizi web geospaziali (WMS, WFS, WCS). Il progetto è mantenuto da Camptocamp, un'azienda nota nel
settore dell'open source geospaziale.

---

## 1. ARCHITETTURA

### Stack Tecnologico e Pattern

- **Linguaggio Principale:** `Dockerfile`. Il progetto non è un'applicazione software tradizionale,
  ma un layer di pacchettizzazione e distribuzione.
- **Pattern Architetturale:** Containerizzazione di un'applicazione monolitica/nativa (QGIS Server).
- **Versioning:** La versione dell'ultima release (`3.44.0`) suggerisce un pattern di _version
  mirroring_, in cui le versioni dell'immagine Docker seguono fedelmente le versioni upstream di
  QGIS (la 3.44 è una versione valida del ramo QGIS).

### Valutazione Manutenibilità

Il progetto ha una lunga storicità (creato nell'ottobre 2016), dimostrando che l'architettura scelta
è stata sostenibile nel tempo. Tuttavia, la natura del progetto (Dockerfile) implica che la
manutenibilità sia strettamente legata alla gestione delle dipendenze di sistema (librerie C++,
GDAL, PROJ) e agli aggiornamenti del sistema operativo di base.

> ⚠️ **[DATO MANCANTE]** Non è possibile determinare dal contesto quale sia l'immagine di base
> utilizzata (es. Debian, Ubuntu, Alpine) né se vengano utilizzati pattern multi-stage build per
> ottimizzare il peso dell'immagine finale, un fattore critico per le performance di deployment in
> ambito GIS.

**Raccomandazioni:**

- Assicurarsi che l'architettura del Dockerfile preveda build multi-stage per ridurre la superficie
  di attacco e il peso dell'immagine, considerando che le librerie GIS native tendono a essere molto
  pesanti.

---

## 2. SICUREZZA

### Metriche e Processi

> ⚠️ **[DATO MANCANTE]** Il punteggio OpenSSF Scorecard non è presente nei dati forniti. Non è
> possibile valutare oggettivamente le policy di sicurezza del repository (es. branch protection,
> token permissions).

Tuttavia, dai dati sui contributor emerge un dettaglio interessante: ci sono **15 contributor
totali, ma solo 9 umani**. Questo indica la presenza di **6 bot**.

- **Inferenza sui processi:** L'alta percentuale di bot suggerisce l'implementazione di automazioni,
  molto probabilmente legate all'aggiornamento delle dipendenze (es. Dependabot, Renovate) o a
  pipeline di CI/CD. Questo è un indicatore positivo per la sicurezza, fondamentale per un'immagine
  Docker esposta sul web.

### Rischi Identificati

1.  **Rischio di obsolescenza delle immagini:** L'ultima release risale al `2025-06-23` (circa 9
    mesi prima della data di estrazione dati). In ambito container, 9 mesi senza una nuova release
    pubblicata espongono gli utenti a vulnerabilità (CVE) scoperte nel frattempo nel sistema
    operativo di base o nelle librerie GIS (es. libgdal).

**Raccomandazioni:**

- **Automazione Security Scanning:** Integrare strumenti come Trivy o Clair nella pipeline per
  scansionare le immagini Docker prima del rilascio.
- **Patching Regolare:** Implementare un rilascio automatico (es. mensile) per aggiornare i
  pacchetti OS base, anche in assenza di nuove versioni di QGIS Server.

---

## 3. QUALITÀ

### Contributor e Bus Factor

Il progetto dichiara un **Bus Factor di 3**, ma l'analisi della distribuzione delle contribuzioni
rivela una forte centralizzazione:

| Contributor   | Commits     | Percentuale |
| :------------ | :---------- | :---------- |
| `@sbrunner`   | 473         | 57.0%       |
| `@yjacolin`   | 11          | 1.3%        |
| Altri 7 umani | 13 (totali) | < 1.5%      |

> ⚠️ **Rischio di continuità:** Sebbene il Bus Factor teorico sia 3, il progetto è di fatto
> mantenuto quasi esclusivamente da `@sbrunner`. Il divario tra il primo e il secondo contributor
> (473 vs 11 commit) indica un forte collo di bottiglia nella conoscenza del progetto (Siloed
> Knowledge).

### Velocity e Gestione Issue

- **Velocity:** Bassa ma costante. Con 2 commit negli ultimi 30 giorni e 4 negli ultimi 90 giorni,
  il progetto è in modalità di "manutenzione passiva".
- **Gestione Issue:** Ci sono **27 Open Issues**. A fronte di una velocity di ~1-2 commit al mese,
  27 issue aperte rappresentano un backlog significativo per un progetto di sola infrastruttura
  Docker. Questo potrebbe indicare difficoltà nel riprodurre bug specifici legati a configurazioni
  GIS complesse o mancanza di tempo da parte del maintainer principale.
- **Rilasci:** Il disallineamento tra l'ultimo commit (`2026-03-11`) e l'ultima release
  (`2025-06-23`) indica che ci sono modifiche nel ramo principale che non sono state pacchettizzate
  e distribuite agli utenti per quasi un anno.

**Raccomandazioni:**

- **Mitigazione Bus Factor:** Incoraggiare altri membri dell'organizzazione Camptocamp a fare code
  review e merge delle PR per distribuire la conoscenza delle configurazioni di QGIS Server.
- **Triage delle Issue:** Effettuare una sessione di pulizia delle 27 issue aperte, chiudendo quelle
  obsolete (es. relative a versioni di QGIS non più supportate).
- **Release Automation:** Automatizzare il processo di rilascio (es. tramite GitHub Actions)
  affinché ogni modifica stabile al `Dockerfile` generi un nuovo tag Docker, riducendo il gap
  temporale tra commit e release.

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
