# wpf

> Migrato da: https://sites.google.com/site/doitsup/documentazione/wpf
> Data migrazione: 2026-05-06

> Pagina originale era placeholder strutturale - migrare contenuto se rilevante recuperandolo dal codice sorgente.

Mappa strutturale dei componenti WPF del framework DoiT.

## Gerarchia dei componenti

```text
wpfConnect
wpfPages
└── wpfPage
    └── wpfSplitter
        ├── wpfPanel(1)
        └── wpfPanel(2)
wpfElement
wpfSection (con overload)
├── wpfSectionTiles
├── wpfSectionTree
└── wpfSectionFields
```

## Componenti UI elencati

- `wpfSplitter`
- `wpfPanel`
- `wpfTabs`
- `wpfElementsContainer`
- `wpfElementsContaner` (variante / probabile typo nel sorgente)

## Classi correlate (lato modello DoiT)

- `cDoSectionEmpty`
- [cDoSectionQuery](./cdosectionquery.md)
- `cDoSectionReports`
- `cDoSectionTabPages`
- `cDoSectionTree`
- [cDoSectionFilter](./cdosection-filter.md)
- `cDoSectionTable`

## Note

La pagina rappresentava una mappa strutturale senza descrizioni tecniche dettagliate dei componenti.

## Vedi anche

- [vmModel](./vmmodel.md)
- [cDoPage](./cdopage.md)
- [cDoSections](./cdosections.md)
