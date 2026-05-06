# Miscellanea — Indice

> Sezione di documentazione legacy migrata da Google Sites Classic (`sites.google.com/site/doitsup/miscellanea/...`) a Markdown in-repo.
> Data migrazione: 2026-05-06

Questa sezione raccoglie pagine di supporto trasversali al framework **DoiT** (CMS data-oriented in VB.NET con frontend Angular): note di rilascio, FAQ, frammenti di codice, riferimenti tecnici e materiale di installazione.

## File migrati

| File | Descrizione |
|---|---|
| [ultimi-aggiornamenti.md](./ultimi-aggiornamenti.md) | Pagina archivio degli aggiornamenti del progetto. Originale vuoto/placeholder — non popolato sul sito Classic. |
| [web-server-crystal.md](./web-server-crystal.md) | Configurazione dei permessi sulla cartella temporanea di Windows necessari per Crystal Reports in modalità web (errore `Load report failed`). Due opzioni: permessi all'application pool o ASP.NET impersonation. |
| [cdosymplyrecordset.md](./cdosymplyrecordset.md) | Esempio completo di uso della classe `cDoSimplyRecordSet` per aggiornamento/inserimento batch di record con `Seek`, `NoMatch`, `Update` e gestione errori. |
| [manuale.md](./manuale.md) | Indice del manuale utente DoiT (Prerequisiti, Installazione, Primo avvio...). Originale era un hub di navigazione con la maggior parte delle sezioni non popolate. |
| [files.md](./files.md) | Pagina File Cabinet — rinviava a una cartella Google Drive (`0B8Fn5q25Tq51TkhEZm1SekhpZzQ`). Nessun allegato esposto in HTML. |
| [news.md](./news.md) | Storico delle versioni / changelog: nuove funzioni di calcolo date, funzioni mail (`AdMail`, `AdMailOf`), proprietà di `DoAmbient`, comportamento pagine modali, miglioramenti `cDoSection`. |
| [webactivity.md](./webactivity.md) | Pagina di tracciamento attività web. Originale rinviava a un Google Sheet esterno. Vuoto/placeholder. |
| [frammenti-codice.md](./frammenti-codice.md) | Indice di una raccolta di 16 snippet (gestione errori, invio mail, esportazione Excel, XAML password, Oracle stored, ecc.). I singoli snippet risiedono in un Google Sheet esterno e non sono stati migrati. |
| [faq.md](./faq.md) | Indice delle FAQ in tre sezioni: Sintassi Oracle, Altro (configurazione SMTP, esportazione, Google Map, immagini in report...) e Script Tips (`cDoRecordDocs`, `cDoRecordSet`, message box, sezioni run time). |
| [documentazione-tecnica.md](./documentazione-tecnica.md) | Sommario della documentazione tecnica del framework: `cDoConnect`, `cDoPage`, `cDoSection` (Query, Filtro, Record, Reports, Treeview, Documenti, Collegamento). |

## Stato della migrazione

- Pagine con contenuto effettivo migrato (5/10): `web-server-crystal`, `cdosymplyrecordset`, `news`, e parzialmente `manuale`, `files`.
- Pagine indice/placeholder preservate come scaffolding (5/10): `ultimi-aggiornamenti`, `webactivity`, `frammenti-codice`, `faq`, `documentazione-tecnica`. Per queste i contenuti di dettaglio sono in sottopagine o risorse esterne non incluse in questa migrazione iniziale.

## Pagine collegate non migrate (out of scope)

- `manuale/webserver` — Configurazione `web.config` (linkata da `manuale.md`)
- 16 sottopagine di `frammenti-codice`
- Sottopagine di `faq` (Sintassi Oracle, Altro, Script Tips)
- Sottopagine di `documentazione-tecnica` (Proprietà / Metodi di `cDoConnect`, `cDoPage`, `cDoSection`)
- Cartella Google Drive `0B8Fn5q25Tq51TkhEZm1SekhpZzQ` (allegati File Cabinet)
