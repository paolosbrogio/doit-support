# WebcDoPage

> Migrato da: https://sites.google.com/site/doitsup/web/webcdopage
> Data migrazione: 2026-05-06

> Pagina originale con contenuto minimale (definizioni di enumerazioni e proprieta'). Migrare contenuto se rilevante / integrare con esempi pratici.

`WebcDoPage` rappresenta la pagina web associata a una `cDoPage` del framework DoiT.

## WebPageMenuMode

Determina come viene visualizzato il menu della pagina. Valori dell'enum `WebEnums.WebPageMenuMode`:

| Valore | Costante | Descrizione |
|---|---|---|
| `1` | `LeftPanel` | Menu visualizzato nel pannello laterale sinistro. |
| `10` | `NoMenu` | Nessun menu visualizzato. |

```vbnet
' Esempio dichiarativo dell'enum (riferimento)
Public Enum WebPageMenuMode
    LeftPanel = 1
    NoMenu = 10
End Enum
```

## Flush

`WebFlush` datatable con i flussi di comunicazione.

## ToolBar Menu

```vbnet
Public cDoConnect.WebcDoPageToolBarMenu As cDoPage
```

E' la pagina web della tool bar associata alla connessione.

## Vedi anche

- [WebSingleton](./websingleton.md)
- [WebStruct](./webstruct.md)
- [Web Methods](./web-methods.md)
