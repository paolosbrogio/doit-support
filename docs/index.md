# Documentazione DoiT

> 📥 Migrato da: https://sites.google.com/site/doitsup/home
> 🗓️ Data migrazione: 2026-05-06
> 📦 Stato: migrazione iniziale completata, contenuti da arricchire dove indicato

DoiT è un **CMS data-oriented** (non solo content-oriented) — abilita la creazione di pagine per operazioni su database con supporto multi-piattaforma (Windows + Web/Angular). Offre scripting di customizzazione e integrazione con webservice.

## Indice generale

### 📘 [Documentazione](./documentazione/README.md) (21 pagine)
Documentazione tecnica delle classi e API del framework.

- 🟢 **Pagine sostanziali**: [startapplication](./documentazione/startapplication.md) (CLI + URL params), [cdorecorddocs](./documentazione/cdorecorddocs.md) (gestione documenti)
- 🟡 **Pagine reference**: [cdohtmlinherited](./documentazione/cdohtmlinherited.md), [cdomails](./documentazione/cdomails.md), [cdotoolbarbuttons](./documentazione/cdotoolbarbuttons.md), [cdowebutility](./documentazione/cdowebutility.md), [cdodownloadfiles](./documentazione/cdodownloadfiles.md)
- 🚧 **Placeholder** (14 pagine vuote sul sito originale, da arricchire): cdoconnect, cdoelements, cdopage, cdosection-filter, cdosectionquery, cdosections, cdoweb, doambient, doitwebservice, general, myio, scripting, vmmodel, wpf

### 🌐 [Web](./web/README.md) (4 pagine)
Specificità della versione Web/Angular del framework.

- 🟢 **Pagine sostanziali**: [web-methods](./web/web-methods.md) (9 metodi/eventi documentati)
- 🚧 **Placeholder**: websingleton, webstruct, webcdopage

### 🗂️ [Miscellanea](./miscellanea/README.md) (10 pagine)
Risorse trasversali, FAQ, snippet, changelog.

- 🟢 **Pagine sostanziali**: [web-server-crystal](./miscellanea/web-server-crystal.md) (config IIS), [cdosymplyrecordset](./miscellanea/cdosymplyrecordset.md) (esempio batch update), [news](./miscellanea/news.md) (changelog 2013-2014), [manuale](./miscellanea/manuale.md) (struttura)
- 🚧 **Placeholder/indice**: ultimi-aggiornamenti, webactivity, files (File Cabinet → Drive), frammenti-codice (16 snippet → Google Sheet), faq (12 domande → Google Sheet), documentazione-tecnica

## Stato della migrazione

| Sezione | Pagine | Sostanziali | Reference | Placeholder |
|---|---|---|---|---|
| Documentazione | 21 | 2 | 5 | 14 |
| Web | 4 | 1 | 0 | 3 |
| Miscellanea | 10 | 4 | 0 | 6 |
| **Totale** | **35** | **7 (20%)** | **5 (14%)** | **23 (66%)** |

### 🚨 Note importanti

1. **2/3 delle pagine erano vuote sul sito originale** — non è "documentazione obsoleta", è scaffolding mai compilato. La migrazione ha preservato la struttura come placeholder per integrazioni future.

2. **Contenuti esterni non migrati** (rimangono come riferimento):
   - **File Cabinet**: cartella Google Drive `0B8Fn5q25Tq51TkhEZm1SekhpZzQ` (allegati legacy)
   - **Frammenti di codice**: Google Sheet `1w7SMW807jT11iNyICTCrPFRdwb0GIgryVW4-nkRv5sY` (16 snippet)
   - **FAQ**: Google Sheet con 12 domande/risposte
   - Da valutare se scaricare e migrare manualmente

3. **Review prioritaria suggerita** (classi nucleari, doc reale è in `.vb`):
   - [`cdoconnect.md`](./documentazione/cdoconnect.md) — classe centrale, urge documentazione dal sorgente
   - [`cdosections.md`](./documentazione/cdosections.md) / [`cdoelements.md`](./documentazione/cdoelements.md) — pilastri del framework
   - [`scripting.md`](./documentazione/scripting.md) — hub eventi (cDoConnect/cDoPage/cDoSection/cDoElement)
   - [`cdopage.md`](./documentazione/cdopage.md) — il body originale parlava di `cDoSectionTemplates`: inconsistenza da chiarire

## Come contribuire

> **Regola fondamentale**: ogni modifica a una funzione pubblica documentata deve aggiornare il `.md` corrispondente **nella stessa commit**.

Per integrare i placeholder con contenuto reale: aprire il file sorgente `.vb` corrispondente (es. `Doit2012/TestTHDom/ThesiVBNET/cObjects/cDoObjects/cDoSection.vb`), estrarre la doc dalle XML doc comments e dalle firme pubbliche, scrivere in Markdown nel file corrispondente.

## Pubblicazione web (futuro)

Quando 50%+ dei file avranno contenuto sostanziale, valutare publishing automatico via:
- **MkDocs Material** (Python, build statico)
- **Docusaurus** (React, search nativo)
- **GitHub Pages** se repo pubblico

---

> ✅ Migrazione iniziale autonoma completata da Claude Code in 3 sub-agent paralleli.
> 🛑 Sito originale Google Sites: lasciare come archivio fino a integrazione completa, poi cancellare.
