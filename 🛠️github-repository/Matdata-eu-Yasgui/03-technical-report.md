---
repo: Matdata-eu/Yasgui
url: https://github.com/Matdata-eu/Yasgui
date_analysis: 2026-03-27
version: 1
analyst: pipeline/report-builder
status: draft
---

# Matdata-eu/Yasgui — Valutazione Tecnica

> **Repository**: [Matdata-eu/Yasgui](https://github.com/Matdata-eu/Yasgui) | **Data analisi**:
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
| Salute     | 🟢 7.8/10 | score composito (attività + BF + issue + release + sec) |
| Attività   | 🟢 Attivo | ultimo commit: 2026-02-28                               |
| Bus Factor | 🟢 4      | contributor dominanti                                   |
| Sicurezza  | ⚪ N/D    | OpenSSF Scorecard                                       |
| CI/CD      | ⚪ N/D    | da topics repo                                          |
| Community  | ⚪ 28     | ★ stars                                                 |

---

## 1. Informazioni Generali

| Campo       | Valore                                                                       |
| ----------- | ---------------------------------------------------------------------------- |
| Repository  | [Matdata-eu/Yasgui](https://github.com/Matdata-eu/Yasgui)                    |
| Categoria   | Frontend                                                                     |
| Licenza     | MIT                                                                          |
| Linguaggio  | TypeScript                                                                   |
| Stars       | 28                                                                           |
| Forks       | 1                                                                            |
| Watchers    | 1                                                                            |
| Open Issues | 15                                                                           |
| Creato      | 2025-12-05 (4 mesi fa)                                                       |
| Archivio    | No                                                                           |
| Fork        | Sì                                                                           |
| Topics      | data, graph, knowledge, linked, rdf, sparql, typescript, webapp, yasgui      |
| Homepage    | https://yasgui.matdata.eu                                                    |
| npm         | [https://www.npmjs.com/package/Yasgui](https://www.npmjs.com/package/Yasgui) |
| DeepWiki    | [deepwiki.com/Matdata-eu/Yasgui](https://deepwiki.com/Matdata-eu/Yasgui)     |

---

## 3. Attività di Sviluppo

| Metrica            | Valore               |
| ------------------ | -------------------- |
| Ultimo commit      | 2026-02-28           |
| Commit (30 giorni) | 10                   |
| Commit (90 giorni) | 10                   |
| Trend commit       | ↑ In crescita        |
| Ultima release     | v5.17.0 (2026-02-28) |

---

## 4. Contribuenti

Totale contributors: **23** (20 umani, 3 bot)

**Bus Factor**: 🟢 4 — contributor con >10% dei commit totali

| #   | Contributor      | Contribuzioni | %     | Tipo |
| --- | ---------------- | ------------- | ----- | ---- |
| 1   | @LaurensRietveld | 556           | 52.9% | User |
| 2   | @MathiasVDA      | 146           | 13.9% | User |
| 3   | @ludovicm67      | 138           | 13.1% | User |
| 4   | @GerwinBosch     | 112           | 10.6% | User |
| 5   | @RossCurry       | 19            | 1.8%  | User |
| 6   | @vemonet         | 13            | 1.2%  | User |
| 7   | @MPvHarmelen     | 5             | 0.5%  | User |
| 8   | @dinikolop       | 5             | 0.5%  | User |
| 9   | @wouterbeek      | 3             | 0.3%  | User |
| 10  | @rubenw          | 3             | 0.3%  | User |
| 11  | @ivan-kovatchev  | 2             | 0.2%  | User |
| 12  | @melvinroest     | 2             | 0.2%  | User |

_... e altri 8 contributors_

---

## 5. Release

| Metrica             | Valore     |
| ------------------- | ---------- |
| Totale release      | 10         |
| Ultima release      | v5.17.0    |
| Data ultima release | 2026-02-28 |

---

## 8. Issues & PR

| Metrica             | Valore |
| ------------------- | ------ |
| Issue aperte        | 15     |
| Issue chiuse (90gg) | 0      |

---

## A1 — Analisi LLM

> _Generata da `pipeline analyze` — fonte: `01-analysis/llm-analysis.md`_

# LLM Analysis: Matdata-eu/Yasgui

**Data:** 2026-03-27 **Sezione:** all **Modello:** gemini-3.1-pro-preview **Data Summary:**
01-data-summary.md

---

Ecco l'analisi tecnica del repository `Matdata-eu/Yasgui`, condotta sulla base dei metadati forniti
e valutata nel contesto dello sviluppo di interfacce per sistemi informativi geospaziali (GIS) e Web
Semantico (GeoSPARQL).

---

## Sintesi del Progetto e Rilevanza GIS

Il progetto si presenta come una "SPARQL development web application". Nel dominio GIS, le
interfacce SPARQL sono componenti architetturali critici per l'interrogazione di knowledge graph
spaziali e layer semantici basati sullo standard OGC **GeoSPARQL**. Un client robusto è essenziale
per la visualizzazione e il testing di query spaziali complesse.

---

## 1. ARCHITETTURA

### Stack Tecnologico e Pattern

- **Linguaggio Principale:** TypeScript.
- **Tipologia:** Web Application.
- **Framework/Librerie specifiche:** [DATO MANCANTE] (Non è possibile determinare dai metadati se
  utilizzi React, Vue, Angular o Web Components nativi).

**Inferenze Architetturali:** L'adozione di **TypeScript** è un indicatore estremamente positivo.
Nello sviluppo di editor di query (come un client SPARQL), la tipizzazione statica riduce
drasticamente i bug a runtime legati al parsing delle stringhe, all'autocompletamento e alla
gestione degli Abstract Syntax Tree (AST).

**Scalabilità e Manutenibilità:**

- **Fatto:** Il progetto è alla versione `v5.17.0` nonostante la data di creazione del repository
  sia recente (Dicembre 2025).
- **Inferenza:** Questo disallineamento temporale suggerisce fortemente che il repository sia una
  migrazione, un fork o il consolidamento di un progetto preesistente molto più maturo. La
  manutenibilità beneficia della maturità del codice (v5+), ma richiede attenzione alla gestione del
  debito tecnico ereditato.

---

## 2. SICUREZZA

> ⚠️ **CRITICITÀ:** I dati relativi all'OpenSSF Scorecard non sono disponibili [DATO MANCANTE]. Non
> è possibile valutare oggettivamente l'implementazione di pratiche di sicurezza automatizzate (es.
> SAST, DAST, dependency scanning).

### Processi e Rischi Identificati

- **Licenza:** MIT (Permissiva, ottima per l'integrazione in stack GIS commerciali e open-source
  senza vincoli di copyleft).
- **Rischio di Dominio (SPARQL):** Essendo un'applicazione web che gestisce query verso endpoint
  esterni, il rischio principale a livello architetturale è legato ad attacchi XSS (Cross-Site
  Scripting) tramite la renderizzazione non sanitizzata dei risultati delle query (es. literal RDF
  contenenti payload malevoli).
- **Gestione Dipendenze:** Non ci sono dati sulla presenza di bot per l'aggiornamento delle
  dipendenze (es. Dependabot).

**Raccomandazioni:**

1. Implementare l'analisi OpenSSF Scorecard per ottenere visibilità sulle pratiche di sicurezza.
2. Verificare l'esistenza di pipeline CI/CD che includano controlli di sicurezza sulle dipendenze
   npm/yarn.

---

## 3. QUALITÀ

### Distribuzione Contributor e Bus Factor

| Metrica                | Valore        | Valutazione                                                              |
| :--------------------- | :------------ | :----------------------------------------------------------------------- |
| **Totale Contributor** | 23 (20 umani) | Molto buona per una nicchia tecnica (SPARQL GUI).                        |
| **Bus Factor**         | 4             | **Sano**. Il progetto sopravviverebbe all'abbandono del main maintainer. |

**Analisi della concentrazione:** Il contributor principale (`@LaurensRietveld`) detiene il 52.9%
dei commit. Tuttavia, la presenza di altri tre core contributor (`@MathiasVDA`, `@ludovicm67`,
`@GerwinBosch`) con percentuali tra il 10% e il 14% dimostra un team distribuito e una conoscenza
del codice condivisa. Questo è un indicatore di alta resilienza del progetto.

### Velocity di Sviluppo e Rilasci

- **Frequenza:** 10 commit negli ultimi 30 giorni (che coincidono con i commit degli ultimi 90
  giorni).
- **Rilasci:** 10 release totali, con l'ultima (`v5.17.0`) effettuata il 2026-02-28 (stessa data
  dell'ultimo commit).
- **Inferenza:** Il progetto ha una velocity moderata ma costante. Il rapporto 1:1 tra commit
  recenti e rilasci suggerisce l'utilizzo di un processo di rilascio automatizzato (es. Semantic
  Release) dove piccoli batch di commit generano versioni stabili.

### Gestione Issue

- **Open Issues:** 15.
- **Metriche Mancanti:** [DATO MANCANTE] Tempo medio di risoluzione (MTTR), numero di issue chiuse,
  presenza di Pull Request aperte/chiuse.
- **Valutazione:** 15 issue aperte a fronte di 28 stars indicano una base utenti attiva che segnala
  bug o richiede feature, ma senza il dato sulle issue chiuse non è possibile valutare la reattività
  dei maintainer.

---

## Conclusioni e Raccomandazioni Azionabili

Il repository `Matdata-eu/Yasgui` appare come un progetto **maturo, tecnicamente solido (TypeScript)
e con un team di sviluppo resiliente (Bus Factor 4)**. È altamente idoneo per l'integrazione in
architetture GIS semantiche per l'interrogazione di endpoint GeoSPARQL.

**Piano d'Azione Consigliato:**

1. **Priorità Alta (Sicurezza):** Abilitare e configurare GitHub Advanced Security (o strumenti
   equivalenti gratuiti per l'open source) per monitorare le vulnerabilità delle dipendenze
   frontend, calcolando l'OpenSSF Scorecard.
2. **Priorità Media (Community):** Analizzare il backlog delle 15 issue aperte per identificare
   eventuali colli di bottiglia nello sviluppo o feature critiche bloccanti per gli utenti.
3. **Priorità Bassa (Documentazione):** Assicurarsi che la documentazione chiarisca il passaggio
   alla versione 5.x, specialmente se il repository è il risultato di una migrazione recente, per
   facilitare l'onboarding di nuovi sviluppatori GIS.

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
