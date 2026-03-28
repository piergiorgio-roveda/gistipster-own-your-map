---
repo: keplergl/kepler.gl
url: https://github.com/keplergl/kepler.gl
date_analysis: 2026-03-26
version: 1
analyst: pipeline/report-builder
status: draft
---

# keplergl/kepler.gl — Valutazione Tecnica

> **Repository**: [keplergl/kepler.gl](https://github.com/keplergl/kepler.gl) | **Data analisi**:
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
| Attività   | 🟢 Attivo | ultimo commit: 2026-03-23                               |
| Bus Factor | 🟡 2      | contributor dominanti                                   |
| Sicurezza  | ⚪ N/D    | OpenSSF Scorecard                                       |
| CI/CD      | ⚪ N/D    | da topics repo                                          |
| Community  | 🟢 11.687 | ★ stars                                                 |

---

## 1. Informazioni Generali

| Campo       | Valore                                                                             |
| ----------- | ---------------------------------------------------------------------------------- |
| Repository  | [keplergl/kepler.gl](https://github.com/keplergl/kepler.gl)                        |
| Categoria   | Frontend                                                                           |
| Licenza     | MIT                                                                                |
| Linguaggio  | TypeScript                                                                         |
| Stars       | 11.687                                                                             |
| Forks       | 1924                                                                               |
| Watchers    | 213                                                                                |
| Open Issues | 610                                                                                |
| Creato      | 2018-02-28 (8 anni fa)                                                             |
| Archivio    | No                                                                                 |
| Fork        | No                                                                                 |
| Topics      | data-visualization, geospatial, kepler, mapbox, visualization                      |
| Homepage    | http://kepler.gl                                                                   |
| npm         | [https://www.npmjs.com/package/kepler.gl](https://www.npmjs.com/package/kepler.gl) |
| DeepWiki    | [deepwiki.com/keplergl/kepler.gl](https://deepwiki.com/keplergl/kepler.gl)         |

---

## 3. Attività di Sviluppo

| Metrica            | Valore              |
| ------------------ | ------------------- |
| Ultimo commit      | 2026-03-23          |
| Commit (30 giorni) | 6                   |
| Commit (90 giorni) | 10                  |
| Trend commit       | ↑ In crescita       |
| Ultima release     | v3.2.6 (2026-03-16) |

---

## 4. Contribuenti

Totale contributors: **30** (29 umani, 1 bot)

**Bus Factor**: 🟡 2 — contributor con >10% dei commit totali

| #   | Contributor                  | Contribuzioni | %     | Tipo |
| --- | ---------------------------- | ------------- | ----- | ---- |
| 1   | @igorDykhta                  | 613           | 38.8% | User |
| 2   | @heshan0131                  | 537           | 34.0% | User |
| 3   | @macrigiuseppe               | 105           | 6.7%  | User |
| 4   | @dariaterekhova-actionengine | 46            | 2.9%  | User |
| 5   | @lixun910                    | 38            | 2.4%  | User |
| 6   | @chrisirhc                   | 16            | 1.0%  | User |
| 7   | @indranildeveloper           | 15            | 1.0%  | User |
| 8   | @akre54                      | 15            | 1.0%  | User |
| 9   | @manassra                    | 14            | 0.9%  | User |
| 10  | @ibgreen                     | 13            | 0.8%  | User |
| 11  | @jonsadka                    | 11            | 0.7%  | User |
| 12  | @ilyabo                      | 10            | 0.6%  | User |

_... e altri 17 contributors_

---

## 5. Release

| Metrica             | Valore     |
| ------------------- | ---------- |
| Totale release      | 10         |
| Ultima release      | v3.2.6     |
| Data ultima release | 2026-03-16 |

---

## 8. Issues & PR

| Metrica             | Valore |
| ------------------- | ------ |
| Issue aperte        | 610    |
| Issue chiuse (90gg) | 0      |

---

## A1 — Analisi LLM

> _Generata da `pipeline analyze` — fonte: `01-analysis/llm-analysis.md`_

# LLM Analysis: keplergl/kepler.gl

**Data:** 2026-03-26 **Sezione:** all **Modello:** gemini-3.1-pro-preview **Data Summary:**
01-data-summary.md

---

Ecco l'analisi tecnica del repository `keplergl/kepler.gl`, basata esclusivamente sui metadati
forniti.

## 1. ARCHITETTURA

### Stack Tecnologico e Pattern Inferibili

- **Linguaggio Principale:** Il progetto è sviluppato in **TypeScript**. L'adozione di un linguaggio
  fortemente tipizzato è una best practice fondamentale per tool di analisi geospaziale, in quanto
  garantisce maggiore robustezza nella manipolazione di strutture dati complesse (es. GeoJSON,
  coordinate, matrici di trasformazione).
- **Dominio e Performance:** La descrizione definisce il tool come ottimizzato per "large-scale data
  sets" e il suffisso ".gl" nel nome suggerisce fortemente un'architettura basata su accelerazione
  hardware (es. WebGL) per il rendering client-side. Questo implica pattern architetturali orientati
  alla gestione efficiente della memoria e al parallelismo (GPU computing).

### Valutazione Scalabilità e Manutenibilità

- **Maturità:** Creato a febbraio 2018, il progetto ha un'architettura consolidata da circa 8 anni
  di sviluppo.
- **Manutenibilità:** L'uso di TypeScript favorisce la manutenibilità a lungo termine. Tuttavia, il
  rapporto tra l'età del progetto e l'attuale velocity solleva dubbi sulla facilità di refactoring
  dell'attuale base di codice.

> ⚠️ **Finding Architetturale:** Il progetto sembra trovarsi in una fase di "maintenance mode" o di
> maturità avanzata, dato il basso numero di commit recenti (10 negli ultimi 90 giorni) a fronte di
> un'alta popolarità.
>
> - **Raccomandazione:** Valutare se l'architettura attuale necessita di un refactoring per
>   abbassare la barriera d'ingresso per nuovi contributor, dato il rallentamento dello sviluppo.

---

## 2. SICUREZZA

### Score OpenSSF e Processi

- **OpenSSF Scorecard:** [DATO MANCANTE] Non sono stati forniti dati relativi alle metriche OpenSSF.
- **Licenza:** Il progetto utilizza licenza **MIT**, che è permissiva e non presenta rischi di
  copyleft per l'integrazione in ambienti enterprise o commerciali.
- **Patching:** La presenza di una release molto recente (`v3.2.6` rilasciata il 2026-03-16) indica
  che, nonostante la bassa frequenza di commit, esiste un processo attivo di rilascio,
  presumibilmente per bugfix o patch di sicurezza.

### Rischi Identificati

- **Rischio di Continuità (Supply Chain):** Il rischio di sicurezza principale derivabile dai dati è
  legato al fattore umano (vedi sezione Qualità). Una dipendenza critica da soli due sviluppatori
  per un pacchetto con quasi 12.000 star rappresenta un rischio per la tempestività di risoluzione
  di eventuali vulnerabilità (CVE).
- **Issue Backlog:** La presenza di 610 issue aperte potrebbe nascondere segnalazioni di
  vulnerabilità non ancora classificate (triage).

> ⚠️ **Finding di Sicurezza:** L'assenza di dati OpenSSF unita a un backlog di 610 issue rappresenta
> un rischio potenziale per la sicurezza.
>
> - **Raccomandazione:** Eseguire un triage prioritario delle 610 issue aperte filtrando per tag
>   legati alla sicurezza. Implementare l'OpenSSF Scorecard per monitorare oggettivamente le
>   pratiche di security del repository.

---

## 3. QUALITÀ

### Maturità e Adozione

Il progetto mostra metriche di adozione eccezionali per il dominio GIS open source:

- **Stars:** 11.687
- **Forks:** 1.924
- Questi numeri indicano che il tool è uno standard de facto o comunque una libreria di riferimento
  nel panorama dell'analisi geospaziale.

### Distribuzione Contributor (Bus Factor)

L'analisi della contribuzione rivela una criticità strutturale significativa:

- **Bus Factor:** **2**.
- **Concentrazione:** I primi due contributor (`@igorDykhta` e `@heshan0131`) gestiscono
  congiuntamente il **72.8%** delle contribuzioni totali.
- C'è un crollo drastico dal terzo contributor in poi (dal 34.0% al 6.7%).

| Fascia Contribuzione | Contributor                                             | % Cumulata |
| :------------------- | :------------------------------------------------------ | :--------- |
| Core (Top 2)         | @igorDykhta, @heshan0131                                | 72.8%      |
| Secondary (Top 3-5)  | @macrigiuseppe, @dariaterekhova-actionengine, @lixun910 | 12.0%      |
| Long Tail (Altri 25) | Vari                                                    | 15.2%      |

### Velocity di Sviluppo e Gestione Issue

- **Velocity:** Estremamente bassa. Solo 6 commit negli ultimi 30 giorni e 10 negli ultimi 90
  giorni. Questo indica che lo sviluppo di nuove feature è quasi fermo.
- **Gestione Issue:** **610 Open Issues**. Questo numero è elevato e, confrontato con la bassa
  velocity (10 commit/90gg), indica un accumulo di debito tecnico o un'incapacità dell'attuale team
  di core maintainer di smaltire il feedback della vasta community (1924 fork).
- **Release Management:** Nonostante la bassa velocity, il progetto segue un versionamento semantico
  (v3.2.6) e ha rilasciato di recente (16 Marzo 2026), dimostrando che la pipeline di CI/CD e il
  processo di release sono funzionanti.

> ⚠️ **Finding di Qualità:** Il progetto soffre di un grave collo di bottiglia gestionale. Un Bus
> Factor di 2 su un progetto con quasi 12k star e 610 issue aperte indica un forte rischio di
> burnout dei maintainer e stagnazione del progetto.
>
> - **Raccomandazione:** È imperativo avviare una campagna di community building per elevare i
>   contributor della fascia "Secondary" (es. `@macrigiuseppe`) al ruolo di core maintainer.
>   Implementare bot per lo stale issue management (es. chiusura automatica di issue inattive) per
>   ridurre il rumore di fondo delle 610 issue aperte.

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
