---
title: Vad är crawling?
---

# Vad är crawling?

*Crawling* = automatiskt hämta & indexera innehåll så att AI:n kan söka i det.

![Crawl-flöde](../assets/images/crawling-flow.png){ width="640" }

---

## Steg-för-steg-flöde

```mermaid
sequenceDiagram
    autonumber
    User->>Intric: Ange källa (URL/filer)
    Intric->>Fetcher: Hämta data
    Fetcher->>Extractor: Extrahera text
    Extractor->>Chunker: Dela upp
    Chunker->>Embedder: Vektorisera
    Embedder->>VectorDB: Spara
```

---

## Praktiska exempel

=== "Webbplats"
    ![Modal](../assets/images/website-modal.png){ width="430" }

    1. **Knowledge** → *Websites* → **Connect website**  
    2. Ange URL, välj *Basic / Deep crawl*  
    3. Klicka **Create website** – status visas som *Synced*.

=== "Filsamling" <a id="ladda-upp-filer"></a>
    1. **Create collection** → namnge  
    2. **Upload files** – drag-and-drop  
       ![Upload](../assets/images/upload-dialog.png){ width="380" }
    3. Klar! Notification → *Analysing…* → *Indexed*.

---

## Vanliga problem & lösningar

| Problem | Trolig orsak | Lösning |
|---------|--------------|---------|
| Tomt index | Inloggning krävs | Lägg till credentials |
| Många irrelevanta sidor | För brett scope | Lägg till filter/allowed paths |
| Långsam crawl | 10 000+ sidor | Begränsa djup eller frekvens |

---

### Relaterade ämnen
- [Vad är RAG?](vad-ar-rag.md)
- [Skapa assistenter](../assistenter/skapa-assistenter.md)
