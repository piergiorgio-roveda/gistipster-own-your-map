---
repo: guildxyz/guild.xyz
url: https://github.com/guildxyz/guild.xyz
date_analysis: 2026-03-27
version: 1
analyst: pipeline/report-builder
status: draft
---

# guildxyz/guild.xyz — Valutazione Tecnica

> **Repository**: [guildxyz/guild.xyz](https://github.com/guildxyz/guild.xyz) | **Data analisi**:
> 2026-03-27 | **Versione**: 1

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
| Salute     | 🔴 3.3/10 | score composito (attività + BF + issue + release + sec) |
| Attività   | 🟢 Attivo | ultimo commit: 2025-11-09                               |
| Bus Factor | 🟢 3      | contributor dominanti                                   |
| Sicurezza  | ⚪ N/D    | OpenSSF Scorecard                                       |
| CI/CD      | ⚪ N/D    | da topics repo                                          |
| Community  | 🟡 3500   | ★ stars                                                 |

---

## 1. Informazioni Generali

| Campo       | Valore                                                                     |
| ----------- | -------------------------------------------------------------------------- |
| Repository  | [guildxyz/guild.xyz](https://github.com/guildxyz/guild.xyz)                |
| Categoria   | Frontend                                                                   |
| Licenza     | —                                                                          |
| Linguaggio  | TypeScript                                                                 |
| Stars       | 3500                                                                       |
| Forks       | 481                                                                        |
| Watchers    | 81                                                                         |
| Open Issues | 34                                                                         |
| Creato      | 2021-09-08 (4 anni fa)                                                     |
| Archivio    | No                                                                         |
| Fork        | No                                                                         |
| Homepage    | https://guild.xyz                                                          |
| DeepWiki    | [deepwiki.com/guildxyz/guild.xyz](https://deepwiki.com/guildxyz/guild.xyz) |

---

## 3. Attività di Sviluppo

| Metrica            | Valore     |
| ------------------ | ---------- |
| Ultimo commit      | 2025-11-09 |
| Commit (30 giorni) | 0          |
| Commit (90 giorni) | 0          |

---

## 4. Contribuenti

Totale contributors: **30** (29 umani, 1 bot)

**Bus Factor**: 🟢 3 — contributor con >10% dei commit totali

| #   | Contributor      | Contribuzioni | %     | Tipo |
| --- | ---------------- | ------------- | ----- | ---- |
| 1   | @BrickheadJohnny | 1791          | 48.3% | User |
| 2   | @dovalid         | 883           | 23.8% | User |
| 3   | @cs-balazs       | 530           | 14.3% | User |
| 4   | @KovJonas        | 197           | 5.3%  | User |
| 5   | @FBalint         | 70            | 1.9%  | User |
| 6   | @dominik-stumpf  | 69            | 1.9%  | User |
| 7   | @TomiOhl         | 36            | 1.0%  | User |
| 8   | @gdn992          | 24            | 0.6%  | User |
| 9   | @zgen-marci      | 20            | 0.5%  | User |
| 10  | @Devidxyz        | 13            | 0.4%  | User |
| 11  | @balintligeti    | 12            | 0.3%  | User |
| 12  | @kef1rke         | 11            | 0.3%  | User |

_... e altri 17 contributors_

---

## 8. Issues & PR

| Metrica             | Valore |
| ------------------- | ------ |
| Issue aperte        | 34     |
| Issue chiuse (90gg) | 0      |

---

## A1 — Analisi LLM

> _Generata da `pipeline analyze` — fonte: `01-analysis/llm-analysis.md`_

# LLM Analysis: guildxyz/guild.xyz

**Data:** 2026-03-27 **Sezione:** all **Modello:** gemini-3.1-pro-preview **Data Summary:**
01-data-summary.md

---

Ecco l'analisi tecnica del repository `guildxyz/guild.xyz`, condotta secondo i principi di
valutazione oggettiva e data-driven, con un focus sulle implicazioni per potenziali integrazioni in
ecosistemi software complessi (inclusi domini GIS/geospaziali, sebbene il dominio nativo del
progetto appaia differente).

---

## Premessa sul Dominio

Dai metadati forniti (Descrizione: _"A tool for token-curated communities"_), il repository si
colloca nel dominio Web3/Blockchain e gestione delle community, non nel dominio GIS puro. Tuttavia,
l'analisi verrà condotta valutando la robustezza del software come potenziale componente di
un'architettura più ampia (es. gestione degli accessi tokenizzati a portali cartografici o dataset
geospaziali).

---

## 1. ARCHITETTURA

### Stack Tecnologico e Pattern

- **Linguaggio Principale:** TypeScript. L'uso di TypeScript è un indicatore positivo per la
  manutenibilità, in quanto la tipizzazione statica riduce gli errori a runtime e facilita il
  refactoring, aspetto cruciale in architetture dati complesse.
- **Pattern Architetturali:** [DATO MANCANTE]. Non avendo accesso al codice sorgente, non è
  possibile determinare se il progetto utilizzi pattern monolitici, a microservizi, o architetture
  serverless.
- **Dipendenze e Framework:** [DATO MANCANTE].

### Valutazione Scalabilità e Manutenibilità

- **Fatti:** Il progetto ha accumulato 3500 stars e 481 fork dal 2021, indicando una forte adozione
  iniziale e una probabile validazione dell'architettura da parte della community.
- **Inferenze:** L'assenza totale di commit negli ultimi 90 giorni (ultimo commit: 09-11-2025
  rispetto alla data di analisi 27-03-2026) suggerisce che l'architettura non sta evolvendo per
  supportare nuovi requisiti o che il progetto ha raggiunto una fase di stagnazione.

**Raccomandazione:** Prima di integrare questo strumento in una stack di produzione, è necessario un
audit del codice sorgente per verificare la compatibilità dei framework TypeScript utilizzati (es.
versioni di Node.js o React) con gli standard aziendali correnti.

---

## 2. SICUREZZA

### Analisi e Processi

- **OpenSSF Scorecard:** [DATO MANCANTE]. Non sono forniti dati sulle metriche standard di
  sicurezza.
- **Processi di Security:** [DATO MANCANTE]. Non è possibile verificare la presenza di pipeline
  SAST/DAST o policy di _vulnerability disclosure_.

### Rischi Identificati

> ⚠️ **RISCHIO CRITICO: Obsolescenza delle Dipendenze (Staleness)** Il repository non registra alcun
> commit da oltre 4 mesi (Novembre 2025 - Marzo 2026). Nell'ecosistema JavaScript/TypeScript (npm),
> le vulnerabilità delle dipendenze transitive vengono scoperte con alta frequenza. L'assenza di
> commit implica che non vengono eseguiti aggiornamenti di sicurezza (es. tramite Dependabot o
> Renovate).

**Raccomandazioni:**

1. Eseguire immediatamente un `npm audit` o `yarn audit` sul repository clonato per quantificare le
   vulnerabilità note (CVE) accumulate negli ultimi mesi.
2. Non esporre questo applicativo su reti pubbliche senza aver prima implementato un fork interno
   per l'applicazione delle patch di sicurezza critiche.

---

## 3. QUALITÀ

### Distribuzione Contributor e Bus Factor

- **Bus Factor:** 3. Questo significa che la perdita di 3 sviluppatori chiave porterebbe allo stallo
  del progetto.
- **Concentrazione del lavoro:** Il contributor principale (`@BrickheadJohnny`) ha prodotto il
  **48.3%** dei commit totali. I primi tre contributor (`@BrickheadJohnny`, `@dovalid`,
  `@cs-balazs`) sommano l'**86.4%** delle contribuzioni.
- **Inferenza:** Il progetto, pur avendo 30 contributor totali, è di fatto mantenuto da un nucleo
  estremamente ristretto (core team). La distribuzione è altamente sbilanciata.

### Velocity di Sviluppo e Maturità

- **Velocity:** Attualmente **nulla**. 0 commit negli ultimi 30 e 90 giorni.
- **Maturità:** Il progetto ha quasi 5 anni di vita (creato a Settembre 2021). Il rapporto tra Stars
  (3500) e Open Issues (34) è apparentemente eccellente (meno dell'1% di issue aperte rispetto alle
  stars).
- **Gestione Issue/PR:** [DATO MANCANTE] sui tempi di risoluzione (MTTR) o sul numero di issue
  chiuse. Tuttavia, le 34 issue attualmente aperte, combinate con l'assenza di commit recenti,
  suggeriscono che il triage e la risoluzione dei bug siano attualmente sospesi.

### Qualità del Codice

- **Metriche di Qualità (Coverage, Code Smells):** [DATO MANCANTE].

**Raccomandazioni:**

1. **Mitigazione Bus Factor:** Se si decide di adottare il software, è imperativo allocare risorse
   interne per studiare la codebase, al fine di non dipendere esclusivamente dal core team originale
   (attualmente inattivo).
2. **Valutazione Fork:** Dato l'alto numero di fork (481), verificare se esiste un fork attivo
   mantenuto dalla community che ha preso in carico lo sviluppo dopo Novembre 2025.

---

## Sintesi per il Decision Maker

Il repository `guildxyz/guild.xyz` è un progetto TypeScript storicamente molto popolare e
supportato, ma che attualmente presenta i chiari sintomi di un **progetto dormiente o abbandonato**.

L'integrazione di questo componente in un'infrastruttura (GIS o generica) è **sconsigliata allo
stato attuale** senza un preventivo fork e un audit di sicurezza delle dipendenze, a causa del
rischio legato alla mancanza di manutenzione attiva negli ultimi 4 mesi e all'elevata concentrazione
della conoscenza in un singolo sviluppatore (quasi 50% dei commit).

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
