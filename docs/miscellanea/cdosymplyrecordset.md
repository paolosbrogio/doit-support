# cDoSymplyRecordSet

> Migrato da: https://sites.google.com/site/doitsup/miscellanea/cdosymplyrecordset
> Data migrazione: 2026-05-06

Questa pagina mostra l'utilizzo della classe `cDoSimplyRecordSet` per operazioni batch di aggiornamento e inserimento record su un database.

## Esempio completo

```vbnet
Dim RecordAggiornati as integer=0
Dim RecordInseriti as integer=0

Try
  dim PanelMsg as string=e.cDoPage("GRIGLIA").StatusBarText(1)
  Dim _cDoSimplyRecordSet as New cDoSimplyRecordSet(e.cDoConnect,"dbo.JDE_FQ19304")

  for each datarow as datarow in e.cDoPage("GRIGLIA").datatable.rows
    Dim UseSeek as Boolean = True

    if UseSeek Then
      _cDoSimplyRecordSet.Seek(datarow("KCOD"),datarow("TD_NUMDOC"),datarow("TD_SERDOC"),datarow("RD_NUMRIG"))
    else
      _cDoSimplyRecordSet("SOKCOO").Value = datarow("KCOD")
      _cDoSimplyRecordSet("SODOCO").Value = datarow("TD_NUMDOC")
      _cDoSimplyRecordSet("SODCTO").Value = datarow("TD_SERDOC")
      _cDoSimplyRecordSet("SOLNID").Value = datarow("RD_NUMRIG")
    end if

    _cDoSimplyRecordSet("SOTRDJ").Value = datarow("DATDOC_JDE")
    _cDoSimplyRecordSet("SOPN").Value = datarow("MESEDOC")
    _cDoSimplyRecordSet("SOFY").Value = datarow("ANNODOC")
    _cDoSimplyRecordSet("SOITWT").Value = datarow("QTAFATTUR")
    _cDoSimplyRecordSet("SOSQOR").Value = datarow("QTASECONDA")
    _cDoSimplyRecordSet("SOAEXP").Value = datarow("IMPORTNETTISSIMO")
    _cDoSimplyRecordSet("SOAEXPE1").Value = datarow("IMPORTLORDO")
    _cDoSimplyRecordSet("SOAN8").Value = datarow("CLIFAT")
    _cDoSimplyRecordSet("SOLITM").Value = datarow("RD_ARTICO")

    if _cDoSimplyRecordSet.NoMatch Then
      RecordInseriti = RecordInseriti+1
    else
      RecordAggiornati = RecordAggiornati+1
    end if

    _cDoSimplyRecordSet.UpDate(true)

    if (RecordAggiornati + RecordInseriti) Mod 100 = 0 Then
      e.cDoPage("GRIGLIA").StatusBarText(1)="Elaborati " & RecordAggiornati + RecordInseriti & " di " & e.cDoPage("GRIGLIA").datatable.rows.count
    end if
  Next

  e.cDoPage("GRIGLIA").StatusBarText(1)=PanelMsg
  dim msg as string="Aggiornati: " & RecordAggiornati & vbcrlf
  msg = msg & "Inseriti: " & RecordInseriti & vbcrlf
  domsgbox (msg)

Catch ex as Exception
  DoMsgbox(ex.Message)
end try
```

## Punti chiave

- Elaborazione **batch** dei record con conteggio separato di aggiornamenti e inserimenti.
- Due strategie di posizionamento del cursore: `Seek(...)` (più conciso) oppure assegnazione manuale dei campi chiave.
- La proprietà `NoMatch` indica se il record cercato non esiste — in tal caso l'`Update(true)` lo inserisce.
- Aggiornamento progressivo della status bar ogni 100 record elaborati.
- Gestione errori con blocco `Try / Catch` e segnalazione tramite `DoMsgbox`.
