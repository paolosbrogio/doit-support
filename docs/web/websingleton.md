# WebSingleton

> Migrato da: https://sites.google.com/site/doitsup/web/websingleton
> Data migrazione: 2026-05-06

> Nota: la pagina originale era estremamente sintetica, con pochi dettagli oltre a una dichiarazione di struttura dati. Si raccomanda di integrare la documentazione con esempi pratici e descrizioni piu' approfondite.

## Struttura e componenti

Il `WebSingleton` espone una collezione di pagine web del CMS DoiT, indicizzate per chiave stringa.

### WebAmbcDoPages

- **Tipo:** `Dictionary(Of String, WebAmbcDoPage)`
- **Ruolo:** dizionario delle pagine web del singleton, accessibili per chiave.

### WebAmbcDoPage

Rappresenta la singola voce del dizionario `WebAmbcDoPages` ed espone:

| Proprieta | Descrizione |
|---|---|
| `cDoConnect` | Connessione associata alla pagina (pagina principale). |
| `cDoPage` | Pagina (contiene sia la pagina principale sia la secondaria). |
| `cDoPages` | Collezione delle pagine collegate. |

## Descrizioni

- **Connessione**: pagina principale.
- **Pagina**: contiene sia la pagina principale sia la secondaria.
- **Template**: rimando alla documentazione correlata.

## Vedi anche

- [WebStruct](./webstruct.md)
- [WebcDoPage](./webcdopage.md)
- [Web Methods](./web-methods.md)
