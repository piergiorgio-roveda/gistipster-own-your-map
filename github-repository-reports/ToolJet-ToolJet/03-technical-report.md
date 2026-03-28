---
repo: ToolJet/ToolJet
url: https://github.com/ToolJet/ToolJet
date_analysis: 2026-03-27
version: 1
analyst: pipeline/report-builder
status: draft
---

# ToolJet/ToolJet — Valutazione Tecnica

> **Repository**: [ToolJet/ToolJet](https://github.com/ToolJet/ToolJet) | **Data analisi**:
> 2026-03-27 | **Versione**: 1

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
| Salute     | 🟡 5.6/10 | score composito (attività + BF + issue + release + sec) |
| Attività   | 🟢 Attivo | ultimo commit: 2026-03-25                               |
| Bus Factor | 🔴 1      | contributor dominanti                                   |
| Sicurezza  | ⚪ N/D    | OpenSSF Scorecard                                       |
| CI/CD      | ⚪ N/D    | da topics repo                                          |
| Community  | 🟢 37.657 | ★ stars                                                 |

---

## 1. Informazioni Generali

| Campo       | Valore                                                                                                                                                                                                                                                                                            |
| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Repository  | [ToolJet/ToolJet](https://github.com/ToolJet/ToolJet)                                                                                                                                                                                                                                             |
| Categoria   | Frontend                                                                                                                                                                                                                                                                                          |
| Licenza     | AGPL-3.0                                                                                                                                                                                                                                                                                          |
| Linguaggio  | JavaScript                                                                                                                                                                                                                                                                                        |
| Stars       | 37.657                                                                                                                                                                                                                                                                                            |
| Forks       | 4980                                                                                                                                                                                                                                                                                              |
| Watchers    | 196                                                                                                                                                                                                                                                                                               |
| Open Issues | 970                                                                                                                                                                                                                                                                                               |
| Creato      | 2021-03-30 (4 anni fa)                                                                                                                                                                                                                                                                            |
| Archivio    | No                                                                                                                                                                                                                                                                                                |
| Fork        | No                                                                                                                                                                                                                                                                                                |
| Topics      | ai-app-builder, docker, hacktoberfest, internal-applications, internal-project, internal-tool, internal-tools, javascript, kubernetes, low-code, low-code-development-platform, low-code-framework, no-code, nodejs, reactjs, self-hosted, typescript, web-development-tools, workflow-automation |
| Homepage    | https://tooljet.com                                                                                                                                                                                                                                                                               |
| npm         | [https://www.npmjs.com/package/ToolJet](https://www.npmjs.com/package/ToolJet)                                                                                                                                                                                                                    |
| DeepWiki    | [deepwiki.com/ToolJet/ToolJet](https://deepwiki.com/ToolJet/ToolJet)                                                                                                                                                                                                                              |

---

## 3. Attività di Sviluppo

| Metrica            | Valore                     |
| ------------------ | -------------------------- |
| Ultimo commit      | 2026-03-25                 |
| Commit (30 giorni) | 10                         |
| Commit (90 giorni) | 10                         |
| Trend commit       | ↑ In crescita              |
| Ultima release     | v3.21.11-beta (2026-03-26) |

---

## 4. Contribuenti

Totale contributors: **30** (30 umani, 0 bot)

**Bus Factor**: 🔴 1 — contributor con >10% dei commit totali

| #   | Contributor         | Contribuzioni | %     | Tipo |
| --- | ------------------- | ------------- | ----- | ---- |
| 1   | @Navaneeth-pk       | 1241          | 11.6% | User |
| 2   | @adishM98           | 1002          | 9.4%  | User |
| 3   | @arpitnath          | 883           | 8.2%  | User |
| 4   | @johnsoncherian     | 839           | 7.8%  | User |
| 5   | @akshaysasidrn      | 662           | 6.2%  | User |
| 6   | @RudraPratik30      | 529           | 4.9%  | User |
| 7   | @kavinvenkatachalam | 525           | 4.9%  | User |
| 8   | @gsmithun4          | 419           | 3.9%  | User |
| 9   | @shah21             | 411           | 3.8%  | User |
| 10  | @shaurya-sharma064  | 401           | 3.7%  | User |
| 11  | @stepinfwd          | 371           | 3.5%  | User |
| 12  | @withshubh          | 362           | 3.4%  | User |

_... e altri 18 contributors_

---

## 5. Release

| Metrica             | Valore        |
| ------------------- | ------------- |
| Totale release      | 10            |
| Ultima release      | v3.21.11-beta |
| Data ultima release | 2026-03-26    |

---

## 8. Issues & PR

| Metrica             | Valore |
| ------------------- | ------ |
| Issue aperte        | 970    |
| Issue chiuse (90gg) | 0      |

---

## A1 — Analisi LLM

> _Generata da `pipeline analyze` — fonte: `01-analysis/llm-analysis.md`_

# LLM Analysis: ToolJet/ToolJet

**Data:** 2026-03-27 **Sezione:** all **Modello:** gemini-3.1-pro-preview **Data Summary:**
01-data-summary.md

---

Ecco l'analisi tecnica del repository `ToolJet/ToolJet`, condotta dalla prospettiva di un valutatore
specializzato in architetture GIS e geospaziali.

Sebbene ToolJet sia una piattaforma generalista (low-code/no-code per tool interni e dashboard), la
valutazione terrà conto della sua potenziale adozione in ecosistemi GIS (es. creazione di dashboard
per la visualizzazione di dati geospaziali, interfacce di data-entry per rilievi sul campo,
integrazione con database spaziali come PostGIS).

---

## 1. ARCHITETTURA

### Stack Tecnologico e Pattern

- **Linguaggio Principale:** JavaScript. Nel contesto GIS, questo suggerisce un'alta compatibilità
  potenziale con le principali librerie di web mapping (es. Leaflet, OpenLayers, MapLibre GL JS) per
  l'estensione delle dashboard.
- **Licenza:** AGPL-3.0. Questo è un fattore architetturale critico. La licenza _Affero General
  Public License_ impone che qualsiasi modifica al software esposta su rete debba essere rilasciata
  con la stessa licenza.
- **Pattern Inferibili:** Essendo una piattaforma per "internal tools" e "AI agents", si deduce
  un'architettura modulare basata su connettori (per database e API) e un motore di rendering UI
  drag-and-drop.

### Valutazione Scalabilità e Manutenibilità

Il progetto gode di un'enorme popolarità (37.657 Stars, 4.980 Forks), il che indica un'architettura
sufficientemente scalabile da aver attratto una vasta adozione. Tuttavia, i dati evidenziano
criticità nella manutenibilità:

- **Backlog elevato:** 970 Open Issues indicano un accumulo significativo di debito tecnico, bug non
  risolti o richieste di funzionalità non gestite.
- **Rilasci:** L'ultima release è una versione beta (`v3.21.11-beta`), il che suggerisce che il ramo
  principale potrebbe contenere codice non ancora stabilizzato per la produzione.

> ⚠️ **Impatto GIS:** L'uso di ToolJet per dashboard geospaziali mission-critical richiede
> attenzione. La licenza AGPL-3.0 impedisce l'inclusione del core modificato in prodotti SaaS
> proprietari senza l'apertura del codice sorgente.

**Raccomandazioni Architetturali:**

- Valutare attentamente l'impatto della licenza AGPL-3.0 prima di integrare ToolJet in architetture
  GIS commerciali.
- Isolare ToolJet come servizio a sé stante (es. tramite container Docker) interfacciandolo ai
  servizi GIS (GeoServer, PostGIS) esclusivamente tramite API standard (REST/GraphQL) per evitare
  contaminazioni di licenza.

---

## 2. SICUREZZA

### Score OpenSSF e Processi

- **OpenSSF Scorecard:** [DATO MANCANTE]. Non è possibile valutare oggettivamente le pratiche di
  sicurezza automatizzate (es. pinning delle dipendenze, token permissions).
- **Processi identificati:** La presenza di rilasci frequenti (ultima release il giorno successivo
  all'ultimo commit registrato) indica una pipeline di CI/CD attiva, ma la natura "beta" dell'ultima
  release richiede cautela.

### Rischi Identificati

1.  **Gestione Credenziali:** Come piattaforma low-code, ToolJet deve memorizzare credenziali per
    database (es. PostGIS) e API (es. Mapbox, Google Maps). Senza dati sulle pratiche di sicurezza,
    questo rappresenta un vettore di attacco primario.
2.  **Vulnerabilità latenti:** L'altissimo numero di Open Issues (970) aumenta statisticamente la
    probabilità che vi siano segnalazioni di sicurezza non ancora triate o patchate.

> ⚠️ **Rischio Critico:** Il Bus Factor riportato è pari a **1**. Sebbene la distribuzione dei
> commit sia spalmata su più sviluppatori, un Bus Factor di 1 indica che una singola persona detiene
> le chiavi dell'infrastruttura, i permessi di merge o le credenziali di rilascio. Questo è un
> rischio inaccettabile per la continuità operativa (Business Continuity) di un progetto enterprise.

**Raccomandazioni di Sicurezza:**

- Implementare un'analisi SAST/SCA indipendente sul codice JavaScript prima dell'adozione.
- Nel contesto GIS, assicurarsi che le connessioni ai database spaziali (es. PostgreSQL/PostGIS)
  avvengano tramite utenti con privilegi minimi (Principio del Least Privilege), limitati in sola
  lettura se la dashboard è solo analitica.

---

## 3. QUALITÀ

### Distribuzione Contributor e Velocity

- **Contributor:** 30 contributori umani identificati. La distribuzione del codice è relativamente
  sana tra i top 10 (il primo contributore ha l'11.6%, il secondo il 9.4%). Questo contraddice
  parzialmente il Bus Factor di 1 a livello di _scrittura del codice_, confermando l'inferenza che
  il collo di bottiglia sia nei permessi di repository/release management.
- **Velocity di Sviluppo:** I dati mostrano un'anomalia severa. Sono registrati **10 commit negli
  ultimi 30 giorni** e **10 commit negli ultimi 90 giorni**. Questo significa che lo sviluppo si è
  fermato per 60 giorni e ha ripreso solo nell'ultimo mese con un volume bassissimo, oppure che il
  team utilizza una strategia di _squash merge_ molto aggressiva che maschera la reale attività.

### Gestione Issue e Maturità

- **Rapporto Issue/Attività:** 970 issue aperte a fronte di soli 10 commit mensili indicano un
  progetto in cui la capacità di risoluzione dei problemi (Issue Resolution Rate) è gravemente
  sbilanciata rispetto alle segnalazioni della community.
- **Maturità:** Nonostante l'alta adozione (37k+ stars), le metriche attuali delineano un progetto
  che sta affrontando una crisi di scalabilità gestionale.

| Metrica Qualitativa    | Valore           | Valutazione                  |
| :--------------------- | :--------------- | :--------------------------- |
| **Community Interest** | 37.657 Stars     | Eccellente                   |
| **Issue Management**   | 970 Open Issues  | Critico (Sotto-dimensionato) |
| **Recent Velocity**    | 10 commit / 90gg | Basso / Anomalo              |
| **Bus Factor**         | 1                | Rischio Estremo              |

> ⚠️ **Impatto GIS:** L'integrazione di formati geospaziali complessi (GeoJSON pesanti, TopoJSON,
> WKT) in piattaforme low-code richiede spesso bug-fixing specifico per ottimizzare le performance
> di rendering. Con una velocity così bassa e un backlog così alto, è improbabile che richieste di
> supporto specifiche per il dominio GIS vengano gestite in tempi utili dal core team.

**Raccomandazioni sulla Qualità:**

- Se si decide di adottare ToolJet per un progetto GIS, è necessario prevedere risorse interne
  capaci di effettuare fork, fixare eventuali bug bloccanti (specialmente legati al parsing di dati
  spaziali in JS) e mantenere una build custom.
- Monitorare il repository per i prossimi 3-6 mesi per verificare se la velocity (10 commit/90gg) è
  un'anomalia temporanea o un segno di abbandono/spostamento verso un modello closed-core.

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
