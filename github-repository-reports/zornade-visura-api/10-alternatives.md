# Alternative: zornade/visura-api

**Data:** 2026-03-26 **Modello:** gemini-3.1-pro-preview

**Candidati analizzati (5):** Guepard-Corp/gfs, c2g-dev/city2graph, qgis/QGIS,
teamapps-org/maplibre-gl-styles, zornade/awesome-italia-opensource

---

### Alternative Dirette

Nessuna alternativa genuina identificata tra i repository candidati.

### Stesso Ecosistema, Scope Diverso

| Repository                          | Differenza di scope                                                                                                                                                 |
| :---------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **c2g-dev/city2graph**              | Si occupa di trasformare relazioni geospaziali in grafi per Machine Learning (GNN) e analisi di rete, mentre il target è un estrattore di dati catastali.           |
| **qgis/QGIS**                       | È un software GIS desktop completo e general-purpose per la visualizzazione e l'analisi spaziale, non un microservizio API per lo scraping di un portale specifico. |
| **teamapps-org/maplibre-gl-styles** | Fornisce stili visivi (frontend) per il rendering di mappe web, ambito completamente slegato dall'estrazione backend di dati tabellari/catastali.                   |

### Note sull'Analisi

L'analisi ha evidenziato che `zornade/visura-api` è uno strumento altamente specializzato: un
wrapper API/scraper (basato su FastAPI e Playwright) progettato esclusivamente per interfacciarsi
con il portale istituzionale italiano SISTER. Nessuno dei candidati proposti risolve questo
specifico problema di approvvigionamento dati. I repository candidati che rientrano nel
macro-dominio geospaziale si occupano di task radicalmente diversi (analisi avanzata con reti
neurali, GIS desktop tradizionale, o styling di mappe web), rendendoli non sovrapponibili né
sostituibili al target. I restanti repository (`Guepard-Corp/gfs` e
`zornade/awesome-italia-opensource`) appartengono a domini del tutto estranei.

---

## ⚠️ Nota sulla Generazione del Contenuto

Questo report è stato generato da un sistema di intelligenza artificiale (LLM:
gemini-3.1-pro-preview).

- **Dati di input**: Profili dei repository estratti deterministicamente dal DB locale
- **Analisi comparativa**: Generata dall'LLM basandosi esclusivamente sui dati sopra indicati
- **Verifica richiesta**: Le relazioni identificate dovrebbero essere verificate prima di decisioni
  critiche — l'LLM non ha accesso al codice sorgente dei repository
