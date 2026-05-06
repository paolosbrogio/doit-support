# cDoRecordDocs

> Migrato da: https://sites.google.com/site/doitsup/documentazione/cdorecorddocs
> Data migrazione: 2026-05-06

Collection di `cDoRecordDoc` per la gestione dei documenti all'interno del framework DoiT.

## Proprieta'

| Proprieta' | Descrizione |
|------------|-------------|
| `DocumentsDataTable` | Restituisce un `DataTable` contenente le colonne con le informazioni dei documenti |
| `Item` | Proprieta' di default che recupera un `cDoRecordDoc` in base alla stringa `PathXmlDataFile` fornita |

## Metodi

### LoadcDoRecordDocs (overload con `PrimaryKeyValues`)

```vbnet
LoadcDoRecordDocs(cDoDbTable, PrimaryKeyValues)
```

Carica i documenti da una tabella di database utilizzando i valori delle chiavi primarie specificate.

### LoadcDoRecordDocs (overload con `cDoSection`)

```vbnet
LoadcDoRecordDocs(cDoDbTable, cDoSection)
```

Carica i documenti da una tabella di database utilizzando i campi chiave primaria estratti da una `cDoSection`.

### OpenCopyDocument

```vbnet
OpenCopyDocument(PathXmlDataFile)
```

Apre una copia del documento specificato e restituisce una stringa contenente il path del file temporaneo.

### SaveNewDocument

```vbnet
SaveNewDocument(DocumentPathSource, DocumentDescription, IsMainDocument, CancelSourceAfterCopy)
```

Persiste un nuovo documento con i metadati forniti e restituisce il corrispondente `cDoRecordDoc`.

### ShowDocument

```vbnet
ShowDocument(PathXmlDataFile)
```

Apre la finestra di gestione del documento. Quando `PathXmlDataFile` e' vuoto, abilita la modalita' inserimento; altrimenti abilita la modalita' modifica.

## Vedi anche

- [Script samples](https://sites.google.com/site/doitsup/miscellanea/domande-frequenti/script-tips/cdorecorddocs_samples) (link esterno: la destinazione non e' in questa sezione migrata)
- `cDoRecordDoc` (sottopagina, non migrata in questa sezione)
