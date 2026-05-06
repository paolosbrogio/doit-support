# Web Server (Crystal Reports)

> Migrato da: https://sites.google.com/site/doitsup/miscellanea/web-server-crysta
> Data migrazione: 2026-05-06

## Premessa

Per utilizzare Crystal Reports in modalità web, l'applicazione richiede i permessi di **lettura e scrittura** sulla directory temporanea di Windows. In mancanza di tali permessi può presentarsi l'errore **"Load report failed"**.

## Soluzioni

A seconda di come è configurato il file `web.config` dell'applicazione, sono disponibili due percorsi alternativi.

### Opzione 1 — Permessi all'utente dell'application pool

Assegnare i permessi di lettura e scrittura all'utente sotto il quale gira l'application pool (ad esempio `IIS_USER`) per la directory temporanea di Windows (ad esempio `C:\Windows\Temp`).

### Opzione 2 — ASP.NET Impersonation

Utilizzare l'impersonation di ASP.NET per gestire l'identità sotto la quale viene eseguita l'applicazione web. Identificare l'identità definita nel file `web.config` e assegnarle i permessi di lettura e scrittura sulla directory temporanea di Windows.

Sintassi di configurazione:

```xml
<identity impersonate="true" userName="<UserName>" password="<UserPassword>" />
```

## Vedi anche

- [Configurazione Web Server (web.config)](./manuale.md) — sezione "Installazione"
