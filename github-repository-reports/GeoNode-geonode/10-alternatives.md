# Alternative: GeoNode/geonode

**Data:** 2026-03-29 **Modello:** gemini-3.1-pro-preview

**Candidati analizzati (4):** geomoose/gm3, geopython/pywps, geoserver/geoserver,
mapbender/mapbender

---

### Alternative Dirette

Nessuna alternativa genuina identificata tra i candidati forniti.

**Motivazione:** GeoNode è una Spatial Data Infrastructure (SDI) completa e un CMS geospaziale che
gestisce l'upload, la catalogazione, la stilizzazione e la condivisione dei dati. Nessuno dei
repository candidati offre questa combinazione di funzionalità full-stack orientate al catalogo e
alla collaborazione.

### Strumenti Complementari

| Repository              | Ruolo nel workflow                        | Motivazione                                                                                                                                                                               |
| :---------------------- | :---------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **geoserver/geoserver** | Motore di pubblicazione dati (Map Server) | GeoServer è il server cartografico standard (WMS/WFS) che viene tipicamente integrato come motore di backend _all'interno_ dell'architettura stessa di GeoNode per il rendering dei dati. |

### Stesso Ecosistema, Scope Diverso

| Repository              | Differenza di scope                                                                                                                                                                                    |
| :---------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **geomoose/gm3**        | È un framework frontend (JavaScript) per la creazione di interfacce web mapping, privo delle funzionalità di backend, gestione utenti e catalogo dati offerte da GeoNode.                              |
| **geopython/pywps**     | È un'implementazione server per lo standard OGC WPS (Web Processing Service) per l'esecuzione di algoritmi, non un portale o un catalogo per la condivisione di dati geospaziali.                      |
| **mapbender/mapbender** | È un framework (PHP) per costruire applicazioni e portali web mapping consumando servizi esistenti, ma non funge da infrastruttura dati (SDI) per l'upload e la gestione dei dati grezzi come GeoNode. |

### Note sull'Analisi

L'analisi si basa sulla distinzione fondamentale nell'ecosistema GIS tra una **Spatial Data
Infrastructure / Spatial CMS** (come GeoNode) e i singoli componenti architetturali. I candidati
forniti rappresentano i "mattoni" di un'architettura GIS (un server cartografico, un server di
processing, framework frontend), mentre GeoNode è la piattaforma di alto livello che spesso
orchestra questi stessi strumenti (in particolare GeoServer) per fornire un prodotto finito agli
utenti finali. Alternative reali a GeoNode sarebbero piattaforme come CKAN (con estensioni spaziali)
o ESRI Geoportal Server.

---

## ⚠️ Nota sulla Generazione del Contenuto

Questo report è stato generato da un sistema di intelligenza artificiale (LLM:
gemini-3.1-pro-preview).

- **Dati di input**: Profili dei repository estratti deterministicamente dal DB locale
- **Analisi comparativa**: Generata dall'LLM basandosi esclusivamente sui dati sopra indicati
- **Verifica richiesta**: Le relazioni identificate dovrebbero essere verificate prima di decisioni
  critiche — l'LLM non ha accesso al codice sorgente dei repository
