# Documentazione DoiT - Indice

> Sezione di documentazione tecnica del framework **DoiT** (CMS data-oriented in VB.NET con frontend Angular).
> Migrazione effettuata da Google Sites (`https://sites.google.com/site/doitsup/documentazione/`) il **2026-05-06**.

## Avvertenza sulla qualita' del contenuto migrato

La maggior parte delle pagine originali risultava **vuota o placeholder**. Solo alcune pagine contenevano materiale sostanziale (`cdorecorddocs.md`, `startapplication.md`). I file marcati `placeholder` mantengono la struttura originale (titolo + sezioni note + "Vedi anche") e dovranno essere ripopolati attingendo al codice sorgente VB.NET.

## Indice dei file migrati

| File | Descrizione | Stato |
|------|-------------|-------|
| [cdoconnect.md](./cdoconnect.md) | Classe centrale di connessione applicativa - hub di accesso a sessione, pagina, sezioni, mail, web utility | placeholder/hub |
| [cdodownloadfiles.md](./cdodownloadfiles.md) | Collection di `cDoDownLoadFile` usata negli script web per ciclare i file scaricabili dall'utente | stub minimale |
| [cdoelements.md](./cdoelements.md) | Dizionario case-insensitive di `cDoElement` (campi/controlli UI) | placeholder/index |
| [cdohtmlinherited.md](./cdohtmlinherited.md) | Imposta i tag HTML degli oggetti DoiT (page, splitter, section, element, column header, table cell) | reference breve |
| [cdomails.md](./cdomails.md) | Collection di `cDoMail` con costruttore `New(cDoConnect)` | placeholder/index |
| [cdopage.md](./cdopage.md) | Classe principale che rappresenta una pagina del framework (contiene sezioni, splitter, scripting) | placeholder/inconsistente |
| [cdorecorddocs.md](./cdorecorddocs.md) | Collection di `cDoRecordDoc` per la gestione documenti (load, open copy, save new, show) | **contenuto sostanziale** |
| [cdosection-filter.md](./cdosection-filter.md) | Variante `cDoSection` per la logica di filtro | vuota/placeholder |
| [cdosectionquery.md](./cdosectionquery.md) | Variante `cDoSection` per esecuzione di query | vuota/placeholder |
| [cdosections.md](./cdosections.md) | Collection delle sezioni (`cDoSection`) di una pagina | hub/placeholder |
| [cdotoolbarbuttons.md](./cdotoolbarbuttons.md) | `ListOf cDoToolBarButton` - bottoni custom della toolbar di sezione | reference minimale |
| [cdoweb.md](./cdoweb.md) | Classe lato web (server / scripting web) del framework | vuota/placeholder |
| [cdowebutility.md](./cdowebutility.md) | Utility web - funzione `WebAlertString(Message As String) As String` | reference minimale |
| [doambient.md](./doambient.md) | Componente di "ambiente" applicativo (configurazioni runtime, contesto) | vuota/placeholder |
| [doitwebservice.md](./doitwebservice.md) | Web Service del framework DoiT | vuota/placeholder |
| [general.md](./general.md) | Funzionalita' trasversali: globali, funzioni di conversione, date | placeholder/in costruzione |
| [myio.md](./myio.md) | Componente per operazioni di I/O custom | vuota/placeholder |
| [scripting.md](./scripting.md) | Indice degli eventi di scripting (`cDoConnect`, `cDoPage`, `cDoSection`, `cDoElement`) | indice/stub |
| [startapplication.md](./startapplication.md) | Avvio dell'applicazione - parametri command line (Window) e URL (Web), `DoItStart.exe` per hot-update | **contenuto sostanziale** |
| [vmmodel.md](./vmmodel.md) | View Model: gerarchia `vmMain` -> `vmPages` -> `vmPage` -> `vmSplitter` -> `vmSection` | stub/placeholder |
| [wpf.md](./wpf.md) | Mappa dei componenti WPF (`wpfConnect`, `wpfPages`, `wpfSection*`, ecc.) | placeholder strutturale |

## Pagine con contenuto sostanziale (migrazione utilizzabile cosi' com'e')

- [cdorecorddocs.md](./cdorecorddocs.md) - proprieta' e metodi documentati
- [startapplication.md](./startapplication.md) - documentazione completa CLI desktop e parametri URL web

## Pagine prioritarie per review umana / ripopolamento

1. [cdoconnect.md](./cdoconnect.md) - classe centrale, deve avere documentazione completa di proprieta' e metodi
2. [cdopage.md](./cdopage.md) - inconsistenza tra titolo e body originale (parlava di `cDoSectionTemplates`)
3. [scripting.md](./scripting.md) - elenca eventi che dovrebbero essere documentati nelle sottopagine
4. [cdosections.md](./cdosections.md), [cdoelements.md](./cdoelements.md) - classi nucleari del framework

## Note di migrazione

- Sottopagine non incluse in questa migrazione (es. `cDoElement`, `cDoToolBarButton`, `cDoRecordDoc`, ecc.) possono essere migrate separatamente.
- Link a risorse esterne (`miscellanea/...`) sono stati mantenuti come URL completo.
- Code samples mantengono syntax highlighting `vbnet` per VB.NET.
