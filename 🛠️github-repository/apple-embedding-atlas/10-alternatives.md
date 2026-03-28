# Alternative: apple/embedding-atlas

**Data:** 2026-03-26 **Modello:** gemini-3.1-pro-preview

**Candidati analizzati (21):** Data-Crew/route-optimizer, GISDATAio/opensourcegisdata,
Guepard-Corp/gfs, Kanahiro/maplibre-vscode-extension, SteveHedden/open-knowledge-graphs,
alibaba/page-agent, c2g-dev/city2graph, do-me/geospatial-atlas, dotbts/BPA, duckdb/duckdb-spatial,
geomatico/maplibre-cog-protocol, geopython/demo.pygeoapi.io, geopython/pygeoapi,
github/awesome-copilot, karpathy/rendergit, microsoft/github-copilot-for-data-science,
moj-analytical-services/uk_address_matcher, opengeospatial/geoparquet, primer/react, qgis/QGIS,
teamapps-org/maplibre-gl-styles

---

### Alternative Dirette

| Repository                 | Linguaggio | Stars | Motivazione                                                                                                                                                        |
| :------------------------- | :--------- | :---- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **do-me/geospatial-atlas** | TypeScript | 134   | Condivide l'esatto scopo primario (visualizzazione interattiva, filtraggio e ricerca di grandi dataset di punti/embedding) e lo stesso stack tecnologico frontend. |

### Strumenti Complementari

| Repository             | Ruolo nel workflow            | Motivazione                                                                                                                                                      |
| :--------------------- | :---------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **c2g-dev/city2graph** | Generazione di dati/embedding | Trasforma relazioni geospaziali in grafi per reti neurali (GNN), generando gli embedding che possono poi essere esplorati visivamente tramite `embedding-atlas`. |

### Stesso Ecosistema, Scope Diverso

| Repository                    | Differenza di scope                                                                                                                                                         |
| :---------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **qgis/QGIS**                 | È un software GIS desktop general-purpose per l'analisi spaziale tradizionale, non un'applicazione web specializzata nell'esplorazione di embedding ad alta dimensionalità. |
| **duckdb/duckdb-spatial**     | È un'estensione backend per l'esecuzione di query spaziali su database, non un'interfaccia frontend per la visualizzazione interattiva.                                     |
| **opengeospatial/geoparquet** | È una specifica di formato per l'archiviazione di dati vettoriali, non uno strumento software per l'esplorazione visiva dei dati.                                           |

### Note sull'Analisi

L'analisi ha evidenziato una forte sovrapposizione tra il target e `do-me/geospatial-atlas`, le cui
descrizioni fornite sono quasi identiche (differiscono solo per i termini "embeddings" e "point
datasets", che nel contesto della visualizzazione 2D/3D sono concettualmente sovrapponibili). La
maggior parte degli altri repository candidati è stata esclusa in quanto appartenente al GIS
tradizionale (database, formati, desktop app) o a domini software completamente slegati (automazione
browser, routing, agenti AI).

---

## ⚠️ Nota sulla Generazione del Contenuto

Questo report è stato generato da un sistema di intelligenza artificiale (LLM:
gemini-3.1-pro-preview).

- **Dati di input**: Profili dei repository estratti deterministicamente dal DB locale
- **Analisi comparativa**: Generata dall'LLM basandosi esclusivamente sui dati sopra indicati
- **Verifica richiesta**: Le relazioni identificate dovrebbero essere verificate prima di decisioni
  critiche — l'LLM non ha accesso al codice sorgente dei repository
