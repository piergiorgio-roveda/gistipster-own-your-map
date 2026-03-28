# Alternative: c2g-dev/city2graph

**Data:** 2026-03-26 **Modello:** gemini-3.1-pro-preview

**Candidati analizzati (5):** Guepard-Corp/gfs, qgis/QGIS, teamapps-org/maplibre-gl-styles,
zornade/awesome-italia-opensource, zornade/visura-api

---

### Alternative Dirette

Nessuna alternativa genuina presente tra i candidati.

### Stesso Ecosistema, Scope Diverso

| Repository                          | Differenza di scope                                                                                                                                                                                                         |
| :---------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **qgis/QGIS**                       | QGIS è un'applicazione desktop GIS general-purpose per la visualizzazione e l'editing, mentre il target è una libreria Python backend altamente specializzata nella preparazione di dati per Graph Neural Networks (GeoAI). |
| **teamapps-org/maplibre-gl-styles** | Si occupa esclusivamente della componente visiva (frontend) per il rendering di mappe web, mentre il target opera nel backend trasformando dati spaziali per l'analisi di rete e il machine learning.                       |
| **zornade/visura-api**              | Sebbene operi nel dominio dei dati territoriali (catasto) usando Python, è un'API per l'estrazione e lo scraping di documenti, non uno strumento di calcolo o trasformazione geometrica per reti neurali.                   |

### Note sull'Analisi

L'analisi si è basata sulla verifica della sovrapposizione degli scopi primari e dell'utenza target.
`c2g-dev/city2graph` è uno strumento di nicchia focalizzato sul _Graph Representation Learning_ e
l'integrazione tra GIS e framework di deep learning (PyTorch/PyG). Nessuno dei candidati forniti
opera in questo specifico segmento della Data Science spaziale. I repository non menzionati nelle
tabelle (`gfs` e `awesome-italia-opensource`) sono stati esclusi in quanto appartengono a domini
tecnologici completamente estranei al GIS o all'AI.

---

## ⚠️ Nota sulla Generazione del Contenuto

Questo report è stato generato da un sistema di intelligenza artificiale (LLM:
gemini-3.1-pro-preview).

- **Dati di input**: Profili dei repository estratti deterministicamente dal DB locale
- **Analisi comparativa**: Generata dall'LLM basandosi esclusivamente sui dati sopra indicati
- **Verifica richiesta**: Le relazioni identificate dovrebbero essere verificate prima di decisioni
  critiche — l'LLM non ha accesso al codice sorgente dei repository
