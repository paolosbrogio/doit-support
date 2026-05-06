# DoiT Support

Documentazione del framework **DoiT** — CMS data-oriented in VB.NET con frontend Angular.

📖 **Sito pubblicato**: https://paolosbrogio.github.io/doit-support/

## Cos'è questo repo

Solo documentazione tecnica del framework DoiT. Il codice sorgente è in un repo separato e privato.

```
docs/
├── index.md            # Home page
├── documentazione/     # API e classi del framework
├── web/                # Specificità versione Web/Angular
└── miscellanea/        # FAQ, snippet, changelog, risorse varie
```

## Come contribuire

### Modifiche veloci (browser)

1. Vai sul [sito pubblicato](https://paolosbrogio.github.io/doit-support/)
2. Click sull'icona ✏️ in alto a destra di qualsiasi pagina (apre il file `.md` su GitHub)
3. Click sulla matita "Edit" → modifica → "Commit changes"
4. Apri Pull Request → in attesa di review → merge → il sito si aggiorna automaticamente in ~2 min

### Modifiche locali (per chi ha clonato)

```bash
git clone https://github.com/paolosbrogio/doit-support.git
cd doit-support
pip install -r requirements.txt
mkdocs serve   # localhost:8000 con live reload
```

Modifica i `.md` in `docs/`, vedi il preview live, poi push/PR.

## Struttura della doc

| Sezione | Contenuto |
|---|---|
| **Documentazione** | API delle classi del framework: `cDoConnect`, `cDoPage`, `cDoSection`, `cDoElement`, `Scripting`, ecc. |
| **Web** | Componenti specifici della versione Web (Angular): `WebSingleton`, `WebMethods`, ecc. |
| **Miscellanea** | FAQ, snippet, changelog, configurazioni IIS, esempi, risorse trasversali |

## Stato della migrazione

La doc è stata migrata dal vecchio Google Sites (`sites.google.com/site/doitsup`) il 2026-05-06. Molte pagine erano placeholder vuoti già nel sito originale: vanno integrate progressivamente con contenuto reale dal sorgente VB.NET.

Pagine attualmente sostanziali:
- [`startapplication`](docs/documentazione/startapplication.md) — CLI + URL params
- [`cdorecorddocs`](docs/documentazione/cdorecorddocs.md) — gestione documenti
- [`web-methods`](docs/web/web-methods.md) — metodi/eventi Web
- [`web-server-crystal`](docs/miscellanea/web-server-crystal.md) — config IIS Crystal
- [`cdosymplyrecordset`](docs/miscellanea/cdosymplyrecordset.md) — esempio batch update
- [`news`](docs/miscellanea/news.md) — changelog 2013-2014

Issues aperte indicano le pagine prioritarie da popolare.

## Tecnologie

- **Markdown** → contenuto sorgente
- **MkDocs Material** → static site generator (Python)
- **GitHub Actions** → build & deploy automatico su push
- **GitHub Pages** → hosting

## Licenza

Documentazione © 2026 Paolo Sbrogiò. Codice sorgente del framework: vedi repo `Dolt` (privato).
