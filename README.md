# Intric Dokumentation

Detta projekt är en MkDocs-dokumentationswebbplats byggd med Material for MkDocs.

## Lokal utveckling

1. Skapa ett Python-virtuellt miljö:
   ```bash
   python3 -m venv .venv
   ```
2. Aktivera miljön:
   ```bash
   source .venv/bin/activate
   ```
3. Installera beroenden:
   ```bash
   pip install mkdocs-material mkdocs-git-revision-date-localized-plugin mkdocs-glightbox
   ```
4. Starta utvecklingsservern:
   ```bash
   mkdocs serve
   ```

## Lägg till ny sida

1. Skapa en ny Markdown-fil i `docs/`-katalogen.
2. Lägg till sidan under `nav:` i `mkdocs.yml`.
3. Kör `mkdocs serve` för att förhandsgranska ändringarna.