# WebStruct

> Migrato da: https://sites.google.com/site/doitsup/web/webstruct
> Data migrazione: 2026-05-06

> Pagina originale era prevalentemente un indice/placeholder di navigazione, senza contenuto descrittivo sostanziale. Migrare contenuto se rilevante.

## Panoramica

`WebStruct` rappresenta la struttura logica di alto livello del modulo web di DoiT. La pagina originale fungeva da punto di accesso alle componenti elencate sotto: i dettagli tecnici sono distribuiti nelle pagine collegate.

## Componenti collegate

| Componente | Descrizione | Riferimento |
|---|---|---|
| `WebSingleton` | Singleton globale che mantiene il dizionario delle pagine web. | [websingleton.md](./websingleton.md) |
| `WebAmbcDoPages` | Dizionario `Dictionary(Of String, WebAmbcDoPage)` delle pagine. | [websingleton.md](./websingleton.md) |
| `WebAmbcDoPage` | Voce del dizionario: connessione + pagina principale/secondaria. | [websingleton.md](./websingleton.md) |
| `cDoConnect` | Connessione (pagina principale). | (interna al framework) |
| `cDoPage` | Pagina (principale o secondaria). | [webcdopage.md](./webcdopage.md) |
| `cDoPages` | Collezione delle pagine. | (interna al framework) |
| `template` | Template di rendering delle pagine. | (interna al framework) |

## Vedi anche

- [WebSingleton](./websingleton.md)
- [WebcDoPage](./webcdopage.md)
- [Web Methods](./web-methods.md)
