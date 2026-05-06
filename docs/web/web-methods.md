# Web Methods

> Migrato da: https://sites.google.com/site/doitsup/web/web-methods
> Data migrazione: 2026-05-06

Elenco dei metodi/eventi web esposti dal framework DoiT lato server, con il file/URL di riferimento e una breve descrizione del trigger.

## Tabella riassuntiva

| Metodo | File / URL | Descrizione |
|---|---|---|
| `OnLoadStartPage` | `StartPage.Htm` | Caricamento della pagina di avvio. |
| `OnSelectConnection` | `StartPage.Htm` | Selezione di una connessione. |
| `OnLoadLoginPage` | `cDoLogin.Htm?conn=x` | Caricamento della pagina di login. |
| `Login` | `cDoLogin.Htm?conn=x` | Login con user/password. |
| `BeforeLoadPage` | `WDoitPage.htm?IdPage=Px` | Prima del caricamento del DOM. |
| `OnLoadPage` | `WDoitPage.htm?IdPage=Px` | Dopo il caricamento del DOM. |
| `ElementClick` | `WDoitPage.htm?IdPage=Px` | Click su elemento clickabile. |
| `OnChangeOperation` | `WDoitPage.htm?IdPage=Px` | Modifica di un campo editabile. |
| `TableServerSide` | (Ajax DataTable) | Chiamata datatable Ajax. |

## Dettaglio dei metodi

### OnLoadStartPage

**File:** `StartPage.Htm`

Pagina di avvio e di selezione della connessione. Le connessioni sono definite in:

```
[DoItTemplates]\doItConnections.ini
```

Se e' presente una sola connessione, viene effettuata la navigazione automatica alla pagina di login.

### OnSelectConnection

**File:** `StartPage.Htm`

Attivato alla selezione della connessione.

### OnLoadLoginPage

**URL:** `cDoLogin.Htm?conn=x`

Pagina di login della connessione (vedi URL).

### Login

**URL:** `cDoLogin.Htm?conn=x`

Attivato quando l'utente tenta di loggarsi con user/password.

### BeforeLoadPage

**URL:** `WDoitPage.htm?IdPage=Px`

Prima che il DOM della pagina venga caricato. Viene "iniettato" il codice HTML nel `document.getElementById('mainDiv').innerHTML`.

```js
document.getElementById('mainDiv').innerHTML = /* html della pagina */;
```

### OnLoadPage

**URL:** `WDoitPage.htm?IdPage=Px`

Dopo che il DOM della pagina e' stato caricato.

### ElementClick

**URL:** `WDoitPage.htm?IdPage=Px`

Attivato quando l'utente nel browser fa click su un elemento "clickabile" (tipicamente link e bottoni).

### OnChangeOperation

**URL:** `WDoitPage.htm?IdPage=Px`

Attivato quando l'utente nel browser modifica un campo editabile (tipicamente input di tipo `text`, dropdown, ecc.).

### TableServerSide

**Tipo:** Ajax DataTable

Chiamata Ajax di una datatable lato server.

## Vedi anche

- [WebSingleton](./websingleton.md)
- [WebStruct](./webstruct.md)
- [WebcDoPage](./webcdopage.md)
