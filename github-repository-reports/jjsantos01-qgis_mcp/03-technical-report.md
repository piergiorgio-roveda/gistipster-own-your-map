---
repo: jjsantos01/qgis_mcp
url: https://github.com/jjsantos01/qgis_mcp
date_analysis: 2026-03-26
version: 1
analyst: pipeline/report-builder
status: draft
---

# jjsantos01/qgis_mcp — Valutazione Tecnica

> **Repository**: [jjsantos01/qgis_mcp](https://github.com/jjsantos01/qgis_mcp) | **Data analisi**:
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
| Salute     | 🔴 2.2/10 | score composito (attività + BF + issue + release + sec) |
| Attività   | 🟢 Attivo | ultimo commit: 2025-10-01                               |
| Bus Factor | 🟡 2      | contributor dominanti                                   |
| Sicurezza  | ⚪ N/D    | OpenSSF Scorecard                                       |
| CI/CD      | ⚪ N/D    | da topics repo                                          |
| Community  | 🟡 866    | ★ stars                                                 |

---

## 1. Informazioni Generali

| Campo       | Valore                                                                       |
| ----------- | ---------------------------------------------------------------------------- |
| Repository  | [jjsantos01/qgis_mcp](https://github.com/jjsantos01/qgis_mcp)                |
| Categoria   | Backend                                                                      |
| Licenza     | —                                                                            |
| Linguaggio  | Python                                                                       |
| Stars       | 866                                                                          |
| Forks       | 132                                                                          |
| Watchers    | 16                                                                           |
| Open Issues | 11                                                                           |
| Creato      | 2025-03-12 (1 anno fa)                                                       |
| Archivio    | No                                                                           |
| Fork        | No                                                                           |
| DeepWiki    | [deepwiki.com/jjsantos01/qgis_mcp](https://deepwiki.com/jjsantos01/qgis_mcp) |

---

## 3. Attività di Sviluppo

| Metrica            | Valore     |
| ------------------ | ---------- |
| Ultimo commit      | 2025-10-01 |
| Commit (30 giorni) | 0          |
| Commit (90 giorni) | 0          |

---

## 4. Contribuenti

Totale contributors: **4** (4 umani, 0 bot)

**Bus Factor**: 🟡 2 — contributor con >10% dei commit totali

| #   | Contributor   | Contribuzioni | %     | Tipo |
| --- | ------------- | ------------- | ----- | ---- |
| 1   | @jjsantos01   | 9             | 69.2% | User |
| 2   | @zacdezgeo    | 2             | 15.4% | User |
| 3   | @andreimirt   | 1             | 7.7%  | User |
| 4   | @richarddunks | 1             | 7.7%  | User |

---

## 8. Issues & PR

| Metrica             | Valore |
| ------------------- | ------ |
| Issue aperte        | 11     |
| Issue chiuse (90gg) | 0      |

---

## A1 — Analisi LLM

> _Generata da `pipeline analyze` — fonte: `01-analysis/llm-analysis.md`_

# LLM Analysis: jjsantos01/qgis_mcp

**Data:** 2026-03-26 **Sezione:** all **Modello:** gemini-3.1-pro-preview **Data Summary:**
01-data-summary.md

---

Ecco l'analisi tecnica del repository `jjsantos01/qgis_mcp` basata sui metadati forniti.

## Sintesi Esecutiva

Il progetto si propone come un bridge innovativo tra i Large Language Models (LLMs) e QGIS Desktop
utilizzando lo standard MCP (Model Context Protocol). I dati mostrano un'anomalia statistica
significativa: **un'altissima trazione della community (866 stars, 132 fork) a fronte di uno sforzo
di sviluppo microscopico (solo 13 commit totali)**. Questo profilo è tipico di una _Proof of Concept
(PoC)_ diventata virale ma attualmente in stato di stagnazione o abbandono.

---

## 1. ARCHITETTURA

### Stack Tecnologico e Pattern Inferibili

- **Linguaggio:** Python. Scelta obbligata e corretta nel dominio GIS per l'interazione con QGIS
  (tramite `PyQGIS`) e standard di fatto per l'ecosistema AI/LLM.
- **Pattern Architetturale:** Basandosi sulla descrizione, il sistema funge da _Adapter/Bridge_.
  Deve tradurre le richieste in linguaggio naturale (via MCP) in chiamate API specifiche di QGIS
  Desktop (geoprocessing, gestione layer, manipolazione canvas).

### Valutazione Manutenibilità e Scalabilità

- **Complessità:** Con un totale di soli 13 commit dall'inizio del progetto, è altamente probabile
  che l'architettura consista in pochi script monolitici piuttosto che in un'architettura modulare
  complessa.
- **Scalabilità:** Essendo legato a "QGIS Desktop", il tool è intrinsecamente limitato a
  un'esecuzione locale/single-user. Non è progettato per scalabilità cloud (per la quale servirebbe
  QGIS Server).

> ⚠️ **Finding Critico:** L'assenza di commit recenti e il bassissimo numero di commit totali
> suggeriscono che il codice non sia strutturato per una manutenzione a lungo termine o per
> l'estensione delle funzionalità.

**Raccomandazioni:**

- Se il progetto deve evolvere oltre la fase di PoC, è necessario un refactoring verso
  un'architettura a plugin standard di QGIS o un demone locale ben strutturato.
- Definire chiaramente nel `README` i limiti architetturali attuali (es. quali tool di geoprocessing
  sono supportati).

---

## 2. SICUREZZA

### Score OpenSSF e Processi

- **OpenSSF Scorecard:** [DATO MANCANTE]
- **Processi di Sicurezza:** Dai dati non emergono evidenze di pipeline CI/CD per l'analisi statica
  (SAST) o la gestione delle dipendenze (es. Dependabot).

### Rischi Identificati

Il dominio di questo progetto (LLM + QGIS Desktop) presenta vettori di attacco critici:

1. **Esecuzione di Codice Arbitrario (RCE):** QGIS Desktop ha accesso completo al file system locale
   e può eseguire script Python. Se l'LLM può generare e far eseguire comandi PyQGIS senza filtri,
   un attacco di _Prompt Injection_ potrebbe compromettere la macchina dell'utente.
2. **Manipolazione Dati Distruttiva:** Un LLM allucinato potrebbe sovrascrivere o cancellare
   shapefile, database GeoPackage o connessioni PostGIS configurate nel desktop dell'utente.

> ⚠️ **Finding Critico:** L'intersezione tra agenti AI autonomi e un software desktop con privilegi
> locali elevati come QGIS richiede barriere di sicurezza rigorose che, in una PoC di 13 commit,
> sono quasi certamente assenti.

**Raccomandazioni:**

- Implementare un sistema di **Human-in-the-Loop (HITL)**: ogni azione distruttiva o di esecuzione
  codice proposta dall'LLM deve richiedere una conferma esplicita dell'utente nella GUI di QGIS.
- Creare un file `SECURITY.md` per avvisare gli utenti dei rischi legati all'uso di LLM con accesso
  al file system locale.
- Implementare una _whitelist_ rigida dei comandi QGIS eseguibili via MCP.

---

## 3. QUALITÀ

### Contributor e Bus Factor

- **Bus Factor:** 2. Il rischio è moderato/alto. Il creatore (`@jjsantos01`) detiene il 69.2% dei
  commit.
- **Distribuzione:** Ci sono 4 contributor totali, ma i contributi di 3 di essi sono marginali (1 o
  2 commit). Questo indica che la community è interessata (132 fork) ma fatica a contribuire
  attivamente al core, probabilmente per mancanza di una roadmap chiara o di issue "good first
  issue".

### Velocity e Maturità

| Metrica                   | Valore       | Analisi                                                                                                                                      |
| :------------------------ | :----------- | :------------------------------------------------------------------------------------------------------------------------------------------- |
| **Età Progetto**          | ~1 anno      | Creato a Marzo 2025, dati raccolti a Marzo 2026.                                                                                             |
| **Ultimo Commit**         | Ottobre 2025 | Il progetto è fermo da quasi 6 mesi.                                                                                                         |
| **Commit 30/90gg**        | 0 / 0        | **Velocity nulla.** Sviluppo completamente bloccato.                                                                                         |
| **Rapporto Issue/Commit** | 11 / 13      | Estremamente sbilanciato. Gli utenti aprono issue (bug/feature request) quasi allo stesso ritmo con cui è stato scritto il codice originale. |

### Gestione Issue e Qualità

Il progetto ha 11 issue aperte. Considerando che non ci sono commit da 6 mesi, è evidente che il
maintainer non sta gestendo il triage o la risoluzione dei bug. Questo porta a un rapido degrado
della fiducia della community, nonostante l'alto numero di star.

> ⚠️ **Finding Critico:** Il progetto è attualmente in stato di **abbandono (dormant)**. L'hype
> iniziale (866 stars) non si è tradotto in un ciclo di sviluppo sostenibile.

**Raccomandazioni:**

- **Gestione Aspettative:** Il maintainer dovrebbe aggiornare il `README` dichiarando esplicitamente
  lo stato del progetto (es. _Archived_, _Proof of Concept_, o _Looking for Maintainers_).
- **Triage:** Passare in rassegna le 11 issue aperte, chiudendo quelle non riproducibili ed
  etichettando le altre per incoraggiare i 132 utenti che hanno fatto un fork a inviare Pull
  Request.

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
