---
repo: onthegomap/planetiler
url: https://github.com/onthegomap/planetiler
date_analysis: 2026-03-26
version: 1
analyst: pipeline/report-builder
status: draft
---

# onthegomap/planetiler — Valutazione Tecnica

> **Repository**: [onthegomap/planetiler](https://github.com/onthegomap/planetiler) | **Data
> analisi**: 2026-03-26 | **Versione**: 1

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
| Attività   | 🟢 Attivo | ultimo commit: 2026-03-26                               |
| Bus Factor | 🟡 2      | contributor dominanti                                   |
| Sicurezza  | ⚪ N/D    | OpenSSF Scorecard                                       |
| CI/CD      | ⚪ N/D    | da topics repo                                          |
| Community  | 🟡 1983   | ★ stars                                                 |

---

## 1. Informazioni Generali

| Campo       | Valore                                                                           |
| ----------- | -------------------------------------------------------------------------------- |
| Repository  | [onthegomap/planetiler](https://github.com/onthegomap/planetiler)                |
| Categoria   | Full Stack                                                                       |
| Licenza     | Apache-2.0                                                                       |
| Linguaggio  | Java                                                                             |
| Stars       | 1983                                                                             |
| Forks       | 173                                                                              |
| Watchers    | 24                                                                               |
| Open Issues | 98                                                                               |
| Creato      | 2021-10-20 (4 anni fa)                                                           |
| Archivio    | No                                                                               |
| Fork        | No                                                                               |
| Topics      | maps, openstreetmap, osm, overture, vector-tiles                                 |
| DeepWiki    | [deepwiki.com/onthegomap/planetiler](https://deepwiki.com/onthegomap/planetiler) |

---

## 3. Attività di Sviluppo

| Metrica            | Valore               |
| ------------------ | -------------------- |
| Ultimo commit      | 2026-03-26           |
| Commit (30 giorni) | 10                   |
| Commit (90 giorni) | 10                   |
| Trend commit       | ↑ In crescita        |
| Ultima release     | v0.10.1 (2026-03-10) |

---

## 4. Contribuenti

Totale contributors: **30** (29 umani, 1 bot)

**Bus Factor**: 🟡 2 — contributor con >10% dei commit totali

| #   | Contributor        | Contribuzioni | %     | Tipo |
| --- | ------------------ | ------------- | ----- | ---- |
| 1   | @msbarry           | 510           | 37.6% | User |
| 2   | @CommanderStorm    | 17            | 1.3%  | User |
| 3   | @bdon              | 16            | 1.2%  | User |
| 4   | @phanecak-maptiler | 15            | 1.1%  | User |
| 5   | @wipfli            | 14            | 1.0%  | User |
| 6   | @zstadler          | 14            | 1.0%  | User |
| 7   | @erik              | 11            | 0.8%  | User |
| 8   | @bbilger           | 6             | 0.4%  | User |
| 9   | @ZeLonewolf        | 6             | 0.4%  | User |
| 10  | @HarelM            | 3             | 0.2%  | User |
| 11  | @farfromrefug      | 3             | 0.2%  | User |
| 12  | @1Ninad            | 2             | 0.1%  | User |

_... e altri 17 contributors_

---

## 5. Release

| Metrica             | Valore     |
| ------------------- | ---------- |
| Totale release      | 10         |
| Ultima release      | v0.10.1    |
| Data ultima release | 2026-03-10 |

---

## 8. Issues & PR

| Metrica             | Valore |
| ------------------- | ------ |
| Issue aperte        | 98     |
| Issue chiuse (90gg) | 0      |

---

## A1 — Analisi LLM

> _Generata da `pipeline analyze` — fonte: `01-analysis/llm-analysis.md`_

# LLM Analysis: onthegomap/planetiler

**Data:** 2026-03-26 **Sezione:** all **Modello:** gemini-3.1-pro-preview **Data Summary:**
01-data-summary.md

---

Ecco l'analisi tecnica del repository `onthegomap/planetiler` basata sui metadati forniti.

---

# Analisi Repository: onthegomap/planetiler

**Contesto di Dominio:** Il progetto si posiziona in una nicchia critica del panorama GIS: la
generazione di vector tiles su scala globale (planet-scale) a partire da dati OpenStreetMap (OSM).
Questo dominio richiede un'estrema efficienza computazionale, gestione ottimizzata dell'I/O e
scalabilità.

## 1. ARCHITETTURA

### Stack Tecnologico e Pattern Inferibili

- **Linguaggio Principale:** Java.
- **Inferenze Architetturali:** La scelta di Java per un tool descritto come "fast" per elaborazioni
  "planet-scale" suggerisce un'architettura fortemente orientata al multi-threading, alla gestione
  efficiente della memoria (heap management) e all'elaborazione parallela dei dati spaziali. È
  altamente probabile l'uso di pattern di tipo _pipeline_ o _MapReduce_ per processare i file PBF di
  OpenStreetMap e generare archivi di tile (es. PMTiles o MBTiles).
- **Licenza:** Apache-2.0. Ottima scelta per l'ecosistema GIS, in quanto permette un'ampia adozione
  sia in ambito open-source che enterprise/commerciale senza i vincoli di licenze copyleft (es.
  GPL).

### Valutazione e Raccomandazioni

- **[DATO MANCANTE]:** Non sono disponibili dati sui framework specifici utilizzati (es. librerie
  per la geometria spaziale come JTS), né sui sistemi di build (Maven/Gradle) o sulla presenza di
  containerizzazione (Docker), fondamentali per il deployment di tool di data-processing.
- **Raccomandazione:** Verificare la presenza di benchmark architetturali documentati. In tool di
  questo tipo, la regressione delle performance è un rischio critico ad ogni aggiornamento delle
  dipendenze.

---

## 2. SICUREZZA

### Processi e Rischi Identificati

- **[DATO MANCANTE]:** Lo score OpenSSF Scorecard non è fornito. Non è possibile valutare
  oggettivamente la presenza di branch protection, pinning delle dipendenze o analisi statiche del
  codice (SAST).

> ⚠️ **RISCHIO CRITICO - Continuità Operativa (Security by Availability):** Sebbene non sia una
> vulnerabilità del codice, il **Bus Factor pari a 2** rappresenta un rischio di sicurezza legato
> alla _business continuity_. In caso di indisponibilità dei maintainer principali, la risoluzione
> di eventuali CVE nelle dipendenze Java (es. librerie di parsing XML/PBF o logging) subirebbe
> ritardi inaccettabili.

### Valutazione e Raccomandazioni

- **Raccomandazione 1:** Implementare (se non presente) l'OpenSSF Scorecard tramite GitHub Actions
  per avere visibilità continua sulla postura di sicurezza.
- **Raccomandazione 2:** Configurare tool di automazione come Dependabot o Renovate per mitigare il
  rischio di vulnerabilità nelle dipendenze, alleggerendo il carico sul maintainer principale.

---

## 3. QUALITÀ

### Maturità e Trazione

Il progetto mostra un'ottima validazione da parte della community GIS:

- **Stars:** 1983 (valore molto alto per un tool di backend GIS specializzato).
- **Forks:** 173 (indica un buon livello di sperimentazione o adattamento da parte di terzi).
- **Longevità:** Creato a fine 2021, è attivo da oltre 4 anni.
- **Versioning:** L'ultima release è la `v0.10.1`. Il progetto non ha ancora raggiunto la major
  release `1.0.0`, il che potrebbe indicare che le API o i formati di configurazione siano ancora
  soggetti a breaking changes.

### Velocity di Sviluppo

- **Ritmo di rilascio:** 10 release totali in ~4.5 anni indicano un ciclo di rilascio ponderato.
  L'ultima release (10 Marzo 2026) dimostra che il progetto è attivamente mantenuto.
- **Anomalia nei Commit:** I dati mostrano 10 commit negli ultimi 30 giorni e _gli stessi 10 commit_
  negli ultimi 90 giorni. Questo inferisce un modello di sviluppo "a scatti" (bursty): il progetto è
  rimasto inattivo per circa due mesi prima di un recente sprint di aggiornamenti, probabilmente in
  concomitanza con la release `v0.10.1`.

### Distribuzione Contributor (Bus Factor)

| Metrica                | Valore  | Analisi                                                                                                                      |
| :--------------------- | :------ | :--------------------------------------------------------------------------------------------------------------------------- |
| **Totale Contributor** | 30      | Discreta partecipazione esterna per un progetto di nicchia.                                                                  |
| **Bus Factor**         | 2       | **Critico.** Il progetto dipende quasi interamente da 1-2 persone.                                                           |
| **Concentrazione**     | Estrema | `@msbarry` domina lo sviluppo (510 commit). Il divario con il secondo contributor (`@CommanderStorm`, 17 commit) è abissale. |

> ⚠️ **FINDING CRITICO - Sostenibilità del Progetto:** Planetiler è di fatto un progetto
> _single-maintainer_ (`@msbarry`) con contributi periferici da parte della community. Nonostante la
> presenza di contributor da organizzazioni note nel settore (es. `@phanecak-maptiler`), la
> conoscenza profonda dell'engine è centralizzata.

### Gestione Issue

- **Open Issues:** 98. Rapportato al numero di star (1983) e all'età del progetto, è un numero
  fisiologico.
- **[DATO MANCANTE]:** Non conoscendo il numero di issue chiuse o il tempo medio di risoluzione
  (MTTR), non è possibile valutare l'efficienza del triage. Tuttavia, con un solo maintainer
  principale, è probabile che le issue si accumulino se non strettamente legate alla roadmap
  principale.

### Valutazione e Raccomandazioni

- **Raccomandazione 1 (Governance):** Per garantire la sopravvivenza a lungo termine del progetto, è
  imperativo avviare un processo di _maintainer on-boarding_. I contributor ricorrenti (es. i top 5)
  dovrebbero essere incoraggiati ad assumere ruoli di code review o triage delle issue.
- **Raccomandazione 2 (Roadmap):** Chiarire i criteri per il raggiungimento della versione `1.0.0`
  per fornire maggiore stabilità alle organizzazioni che dipendono da questo tool per le loro
  pipeline di dati cartografici.

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
