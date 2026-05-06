# StartApplication

> Migrato da: https://sites.google.com/site/doitsup/documentazione/startapplica
> Data migrazione: 2026-05-06

Documentazione delle modalita' di avvio dell'applicazione DoiT, sia in versione Window (desktop) sia in versione Web.

## Versione Window

L'avvio del programma accetta una stringa di parametri di lancio separati da virgole.

Se il parametro e' un file di tipo `cDoStartScripting`, viene eseguito il codice contenuto nel file:

```text
[ApplicationDirectory]\DoIt.exe \\server\Batch\MioFile.DoStartScripting
```

Altrimenti i parametri sono posizionali:

- **Primo parametro**: path del file `xcDoConnection`
- **Secondo parametro**: utente di connessione
- **Terzo parametro**: password di connessione
- **Quarto parametro**: pagina di startup (se omessa, viene aperta la pagina di startup standard)

```text
[ApplicationDirectory]\DoIt.exe \\server\Connection\MiaConnessione.xcDoConnection,Mario,pwdMario77,MiaPagina.cDoPage
```

### Avvio tramite DoItStart.exe

Utilizzare `DoItStart.exe` al posto di `DoIt.exe` consente gli aggiornamenti "a caldo" dell'applicazione.

`DoItStart` segue l'ordine di avvio definito nel file `DoItStart.ini` sotto la sezione `[StartApplicationOrder]`.

Le opzioni di lancio rimangono le stesse descritte sopra:

```text
[ApplicationDirectory]\DoItStart.exe \\server\Batch\MioFile.DoStartScripting
```

Per l'avvio tipo batch:

```text
[ApplicationDirectory]\DoItStart.exe \\server\Connection\MiaConnessione.xcDoConnection,Mario,pwdMario77,MiaPagina.cDoPage
```

## Versione Web

Tutti i parametri desiderati possono essere passati nella stringa URL di avvio. In particolare:

| Parametro | Descrizione |
|-----------|-------------|
| `cDoConnect` | Nome della connessione (dal file `DoItConnections.ini`) |
| `cDoUid` | Utente di connessione |
| `cDoPwd` | Password di connessione (deprecato - passa la password in chiaro) |
| `cDoStartPage` | Pagina di startup (se omessa, viene aperta la pagina di startup standard) |

Esempio:

```text
http://[DoItWebSite]/?cdoconnect=ThBusiness&cDoStartPage=RdoRig_Forn_update&IdRdoRig=10
```

I parametri custom possono essere recuperati nello scripting tramite la funzione `UrlParams` dell'oggetto `cDoConnect`:

```vbnet
Dim _IdRdoRig As String = e.cDoConnect.UrlParams("IdRdoRig") ' Restituisce 10 nell'esempio sopra
```

## Vedi anche

- [cDoConnect](./cdoconnect.md)
- [cDoPage](./cdopage.md)
