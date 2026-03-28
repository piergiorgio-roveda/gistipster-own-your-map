# Quick Eval: onthegomap/planetiler

**Data:** 2026-03-26 **Modello:** gemini-3.1-pro-preview **Data Summary:** 01-data-summary.md

---

### Sintesi

Planetiler è un generatore ad alte prestazioni basato su Java per la creazione rapida di vector
tiles su scala globale da dati OpenStreetMap, ben consolidato nel panorama GIS ma fortemente
dipendente dal suo creatore.

### Punti di Forza

- **Forte validazione della community:** Ottima adozione per un tool di nicchia, con 1983 stars e
  173 fork.
- **Manutenzione attiva:** Sviluppo costante con commit recentissimi (ultimo al 26/03/2026) e una
  release recente (v0.10.1 rilasciata a marzo 2026).
- **Licenza Enterprise-friendly:** Rilasciato sotto Apache-2.0, privo di vincoli virali per
  l'adozione commerciale.
- **Ecosistema aziendale:** Presenza di contributor legati ad aziende del settore (es.
  `@phanecak-maptiler`), che indica un interesse industriale verso il tool.

### Rischi e Criticità

- **Bus Factor critico:** Il progetto ha un Bus Factor pari a 2. Il lead developer (`@msbarry`)
  domina in modo schiacciante lo sviluppo con 510 contribuzioni, contro le sole 17 del secondo
  contributore.
- **Falsa community distribuita:** Nonostante i 30 contributor totali, 28 di questi hanno un impatto
  marginale (≤ 1.3% dei commit ciascuno), rendendo il progetto di fatto un "one-man show" supportato
  da patch minori.
- **Carico di issue:** 98 issue aperte rappresentano un volume discreto da smaltire per un team core
  così ridotto, potendo indicare potenziali colli di bottiglia nella risoluzione dei bug.

### Raccomandazione

**Valutare con cautela** Il tool risolve un problema tecnico complesso in modo efficiente ed è
attivamente mantenuto, ma l'estrema centralizzazione dello sviluppo su un singolo individuo
rappresenta un rischio sistemico per l'integrazione in architetture enterprise mission-critical a
lungo termine.

### Punteggio

**3.8 / 5.0** — Eccellente utilità, adozione e frequenza di rilascio, ma severamente penalizzato dal
rischio legato al Bus Factor.

---

## ⚠️ Nota sulla Generazione del Contenuto

Questo report è stato generato in parte o nella sua totalità da un sistema di intelligenza
artificiale (LLM: gemini-3.1-pro-preview).

- **Dati di input**: Metadati, commit, issue e metriche raccolte deterministicamente dalle API
  GitHub
- **Analisi qualitativa**: Generata dall'LLM basandosi esclusivamente sui dati sopra indicati
- **Verifica richiesta**: Le valutazioni e conclusioni dovrebbero essere verificate da un revisore
  umano prima di essere utilizzate per decisioni critiche
