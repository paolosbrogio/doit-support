# News

> Migrato da: https://sites.google.com/site/doitsup/miscellanea/versions
> Data migrazione: 2026-05-06

Storico delle nuove funzionalità rilasciate sulla piattaforma DoiT.

## marzo 2014

Aggiunte nuove funzioni e proprietà:

- Funzioni di calcolo date (documentate in **General**):
  - `FirstDayOfMonth`
  - `FirstDayOfPreviousMonth`
  - `FirstDayOfNextMonth`
  - `LastDayOfMonth`
  - `LastDayOfPreviousMonth`
  - `LastDayOfNextMonth`
- Funzioni mail (documentate in **cDoConnect**):
  - `AdMail`
  - `AdMailOf`
- Nuove proprietà su `DoAmbient`:
  - `StartFromcDoStartScripting`
  - `UseMailInsteadDoMsgBox`
- Nuovo metodo su `cDoElement`:
  - `ExecuteClickEvent`

## luglio 2013

**Comportamento delle pagine modali.** Quando viene aperta una pagina modale, tutte le altre pagine vengono disabilitate e non risultano selezionabili — un comportamento più stringente di quello fornito di default dal .NET Framework.

## giugno 2013

Diversi miglioramenti implementati:

- Nuove proprietà su `cDoSection` (Query):
  - `SaveMailMergeParamsOnSeparateFile` — consente di salvare i template di mail merge come file separati anziché incorporati nella pagina.
  - `SaveExcelExportParamsOnSeparateFile` — consente di salvare i parametri di esportazione Excel come file separati anziché incorporati nella pagina.
- Percorso del file `.mdb` di prototipo (usato per creare/modificare i Crystal Report) ora **modificabile dall'utente**.
- Nella finestra di scripting è disponibile un link diretto alla documentazione di aiuto.
- È possibile inserire **pulsanti comando custom** in ciascuna sezione (vedi documentazione `cDoToolBarButtons`).
