---
repo: nextgis/quickmapservices
url: https://github.com/nextgis/quickmapservices
date_analysis: 2026-03-26
version: 1
analyst: pipeline/report-builder
status: draft
---

# nextgis/quickmapservices — Valutazione Tecnica

> **Repository**: [nextgis/quickmapservices](https://github.com/nextgis/quickmapservices) | **Data
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
| Salute     | 🟢 7.8/10 | score composito (attività + BF + issue + release + sec) |
| Attività   | 🟢 Attivo | ultimo commit: 2026-03-11                               |
| Bus Factor | 🟢 4      | contributor dominanti                                   |
| Sicurezza  | ⚪ N/D    | OpenSSF Scorecard                                       |
| CI/CD      | ⚪ N/D    | da topics repo                                          |
| Community  | ⚪ 186    | ★ stars                                                 |

---

## 1. Informazioni Generali

| Campo       | Valore                                                                                 |
| ----------- | -------------------------------------------------------------------------------------- |
| Repository  | [nextgis/quickmapservices](https://github.com/nextgis/quickmapservices)                |
| Categoria   | Plugin                                                                                 |
| Licenza     | GPL-2.0                                                                                |
| Linguaggio  | Python                                                                                 |
| Stars       | 186                                                                                    |
| Forks       | 53                                                                                     |
| Watchers    | 20                                                                                     |
| Open Issues | 25                                                                                     |
| Creato      | 2014-11-24 (11 anni fa)                                                                |
| Archivio    | No                                                                                     |
| Fork        | No                                                                                     |
| Homepage    | https://plugins.qgis.org/plugins/quick_map_services/                                   |
| PyPI        | [https://pypi.org/project/quickmapservices](https://pypi.org/project/quickmapservices) |
| DeepWiki    | [deepwiki.com/nextgis/quickmapservices](https://deepwiki.com/nextgis/quickmapservices) |

---

## 3. Attività di Sviluppo

| Metrica            | Valore             |
| ------------------ | ------------------ |
| Ultimo commit      | 2026-03-11         |
| Commit (30 giorni) | 1                  |
| Commit (90 giorni) | 1                  |
| Trend commit       | ↑ In crescita      |
| Ultima release     | 1.1.0 (2025-12-03) |

---

## 4. Contribuenti

Totale contributors: **23** (23 umani, 0 bot)

**Bus Factor**: 🟢 4 — contributor con >10% dei commit totali

| #   | Contributor          | Contribuzioni | %     | Tipo |
| --- | -------------------- | ------------- | ----- | ---- |
| 1   | @yellow-sky          | 154           | 29.7% | User |
| 2   | @simgislab           | 95            | 18.3% | User |
| 3   | @alisovenko          | 59            | 11.4% | User |
| 4   | @ivanbarsukov        | 52            | 10.0% | User |
| 5   | @514ckw4r3           | 50            | 9.6%  | User |
| 6   | @RemeshevskiyValeriy | 43            | 8.3%  | User |
| 7   | @drnextgis           | 15            | 2.9%  | User |
| 8   | @MatzFan             | 10            | 1.9%  | User |
| 9   | @agiudiceandrea      | 7             | 1.3%  | User |
| 10  | @Rungee              | 7             | 1.3%  | User |
| 11  | @ArtLod              | 6             | 1.2%  | User |
| 12  | @culebron            | 4             | 0.8%  | User |

_... e altri 11 contributors_

---

## 5. Release

| Metrica             | Valore     |
| ------------------- | ---------- |
| Totale release      | 3          |
| Ultima release      | 1.1.0      |
| Data ultima release | 2025-12-03 |

---

## 8. Issues & PR

| Metrica             | Valore |
| ------------------- | ------ |
| Issue aperte        | 25     |
| Issue chiuse (90gg) | 0      |

---

## A1 — Analisi LLM

> _Generata da `pipeline analyze` — fonte: `01-analysis/llm-analysis.md`_

# LLM Analysis: nextgis/quickmapservices

**Data:** 2026-03-26 **Sezione:** all **Modello:** gemini-3.1-pro-preview **Data Summary:**
01-data-summary.md

---

Ecco l'analisi tecnica del repository `nextgis/quickmapservices` basata sui metadati forniti.

---

# Analisi Repository: nextgis/quickmapservices

**Contesto del Progetto:** Il repository ospita un plugin per il software desktop QGIS, progettato
per facilitare la ricerca e l'integrazione di servizi di mappe web (presumibilmente basemaps, WMS,
WMTS, XYZ tiles) all'interno dei progetti GIS. Il progetto è maturo, essendo stato creato nel 2014.

---

## 1. ARCHITETTURA

### Stack Tecnologico e Struttura

- **Linguaggio Principale:** Python.
- **Ecosistema:** Essendo un plugin QGIS, l'architettura è intrinsecamente legata alle librerie
  **PyQGIS** (l'API Python di QGIS) e verosimilmente a **PyQt/PySide** per la gestione
  dell'interfaccia utente (GUI).
- **Pattern Architetturali Inferibili:** Il progetto segue il pattern architetturale standard dei
  plugin QGIS (struttura a moduli con file di inizializzazione `__init__.py` e metadati
  `metadata.txt`). Dal punto di vista funzionale, agisce come un _Client/Aggregator_ che si
  interfaccia con API e servizi web esterni per recuperare cataloghi di mappe e layer spaziali.

### Valutazione Manutenibilità

- **Stabilità vs Obsolescenza:** Il progetto ha oltre 11 anni di vita. L'uso di Python in ambito
  QGIS garantisce una buona leggibilità, ma i plugin storici spesso accumulano debito tecnico legato
  alle transizioni di major release di QGIS (es. da QGIS 2 a QGIS 3).
- **Licenza:** L'utilizzo della licenza **GPL-2.0** è perfettamente allineato con l'ecosistema QGIS
  (anch'esso GPL), garantendo assenza di conflitti legali nell'integrazione.

> ⚠️ **Rischio Architetturale:** La dipendenza da servizi web esterni (cataloghi di mappe) implica
> che l'architettura deve essere resiliente a timeout, link interrotti o cambiamenti nelle API di
> terze parti.

---

## 2. SICUREZZA

### Metriche e Processi

- **OpenSSF Scorecard:** `[DATO MANCANTE]` - Non sono forniti dati relativi a scansioni di sicurezza
  automatizzate o score OpenSSF.
- **Processi identificati:** Dai dati forniti non emergono evidenze di pipeline CI/CD orientate alla
  sicurezza (es. SAST, DAST o dependency scanning).

### Rischi Identificati (Contesto GIS Desktop)

Sebbene sia un'applicazione desktop e non un servizio web esposto, la natura del plugin ("Find and
add map services") introduce vettori di rischio specifici:

1.  **Gestione di URL non attendibili:** Il plugin processa URL esterni. Se non validati
    correttamente, potrebbero esporre l'utente a rischi di SSRF (Server-Side Request Forgery) locale
    o al download di payload malevoli mascherati da servizi GIS.
2.  **Supply Chain:** L'assenza di aggiornamenti frequenti (vedi sezione Qualità) aumenta il rischio
    che eventuali dipendenze Python di terze parti contengano vulnerabilità note (CVE) non patchate.

**Raccomandazioni di Sicurezza:**

- Implementare GitHub Actions per l'analisi statica del codice Python (es. _Bandit_).
- Assicurarsi che il parsing degli endpoint dei servizi mappa (XML/JSON) sia protetto contro
  attacchi come le _XML External Entities (XXE)_, comuni nel parsing di capabilities WMS/WFS.

---

## 3. QUALITÀ

### Distribuzione Contributor (Bus Factor)

Il progetto mostra una distribuzione della conoscenza sorprendentemente sana per un plugin di
nicchia.

| Metrica                | Valore       | Valutazione                                                                                                            |
| :--------------------- | :----------- | :--------------------------------------------------------------------------------------------------------------------- |
| **Totale Contributor** | 23           | Eccellente per un plugin QGIS specifico.                                                                               |
| **Bus Factor**         | 4            | Molto buono. Il progetto non dipende da un singolo sviluppatore.                                                       |
| **Concentrazione**     | Top 4 = ~69% | Fisiologica. `@yellow-sky` guida il progetto (29.7%), ma c'è un solido supporto da parte di altri tre core maintainer. |

### Velocity e Gestione Rilasci

I dati mostrano un progetto in evidente stato di **maintenance mode** (manutenzione passiva) o
stagnazione.

| Metrica                | Valore           | Analisi                                                                                                                                        |
| :--------------------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| **Commit ultimi 90gg** | 1                | Sviluppo attivo praticamente fermo.                                                                                                            |
| **Ultima Release**     | 1.1.0 (Dic 2025) | Rilasci estremamente rari (solo 3 in totale su GitHub, sebbene i rilasci effettivi possano avvenire sul repository ufficiale dei plugin QGIS). |
| **Open Issues**        | 25               | A fronte di 1 commit in 3 mesi, un backlog di 25 issue indica che i bug o le richieste di feature si stanno accumulando senza essere smaltiti. |

> ⚠️ **Criticità di Qualità:** La bassissima velocity (1 commit negli ultimi 90 giorni) combinata
> con 25 issue aperte suggerisce che il team di maintainer (probabilmente legato all'organizzazione
> `nextgis`) ha ridotto drasticamente le risorse allocate al progetto. Questo rappresenta un rischio
> per la compatibilità futura con le nuove versioni di QGIS.

---

## Sintesi e Raccomandazioni Azionabili

Il repository `nextgis/quickmapservices` ospita un plugin storico, molto popolare (186 stars) e con
una base di contributor storicamente ben distribuita. Tuttavia, i dati attuali indicano un forte
rallentamento dello sviluppo.

**Piano d'Azione Consigliato per i Maintainer:**

1.  **Triage del Backlog (Sforzo: Basso | Impatto: Medio):** Analizzare le 25 issue aperte. Chiudere
    quelle obsolete (es. relative a vecchie versioni di QGIS) e taggare le rimanenti per
    identificare bug critici vs feature request.
2.  **Automazione CI/CD (Sforzo: Medio | Impatto: Alto):** Implementare GitHub Actions per testare
    automaticamente il plugin contro le versioni LTR (Long Term Release) e PR (Point Release)
    correnti di QGIS. Questo ridurrà il carico di manutenzione manuale.
3.  **Security Audit Leggero (Sforzo: Basso | Impatto: Alto):** Integrare strumenti come Dependabot
    per monitorare le dipendenze Python e configurare controlli base per la validazione degli URL
    dei servizi mappa gestiti dal plugin.

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
