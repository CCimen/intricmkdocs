---
title: Vad är crawling?
---

# Vad är crawling?

Crawling är processen att hämta in och indexera innehåll från webbplatser, dokument eller API:er för att skapa en sökbar kunskapsbas. I Intric används crawling främst för att ge assistenter tillgång till uppdaterad och relevant information från interna och externa källor.

Med crawling kan du:
- **Samla data:** Läs in text, webb- och filresurser.
- **Indexera innehåll:** Skapa vektorrepresenteringar via embeddings.
- **Säker sökning:** Gör kunskapsbasen tillgänglig för dina AI-assistenter.

[![Crawling-exempel](assets/images/crawling-exempel.png)](assets/images/crawling-exempel.png)
*Exempel på hur man kan ställa in crawling i Intric.*

## Hur crawling fungerar i Intric

Crawling i Intric involverar flera steg som omvandlar webbinnehåll till kunskap som assistenter kan använda:

1. **Datainhämtning:** Systemet besöker angivna webbadresser och hämtar innehåll.
2. **Innehållsextrahering:** Relevant text extraheras från HTML och andra format.
3. **Segmentering:** Innehållet delas upp i mindre, hanterbara segment.
4. **Vektorisering:** Segmenten omvandlas till numeriska vektorrepresentationer (embeddings).
5. **Indexering:** Vektorerna lagras i en databas, redo att sökas baserat på relevans.
6. **Koppling:** Den indexerade kunskapen kopplas till en eller flera assistenter.

!!! info "Embeddings"
    Embeddings är numeriska representationer av text som fångar dess semantiska betydelse. De gör det möjligt att söka efter innehåll baserat på mening och kontext, inte bara nyckelord.

När assistenten sedan får en fråga som kräver information från kunskapsbasen:

1. Frågan konverteras till en embedding
2. Systemet hittar de mest relevanta segmenten i kunskapsbasen
3. Relevanta segment skickas till AI-modellen tillsammans med frågan
4. Assistenten svarar baserat på den kombinerade informationen

## Webbaserad kunskapsinhämtning (Web crawling)

### Förberedelser för effektiv crawling

Innan du startar en crawling-process, överväg följande:

- **Sidans struktur:** Webbplatser med tydlig struktur ger bättre resultat
- **Innehållsmängd:** Större webbplatser kan kräva selektiv crawling
- **Uppdateringsfrekvens:** Hur ofta innehållet ändras påverkar hur ofta du behöver uppdatera kunskapsbasen
- **Rättigheter:** Säkerställ att du har tillstånd att crawla innehållet

### Steg för att crawla en webbplats

1. **Navigera till Kunskapskällor:** Gå till sektionen för kunskapskällor i Intric.
2. **Välj "Lägg till webbplats":** Starta processen för att crawla en ny webbplats.
3. **Ange URL:** Skriv in webbplatsens huvudadress (t.ex. `https://exempel.se`).
4. **Konfigurera crawling-djup:**
   - **Grundläggande (1 nivå):** Endast den specifika sidan hämtas
   - **Måttlig (2-3 nivåer):** Huvudsidan samt direktlänkade sidor
   - **Djup (4+ nivåer):** Omfattande crawling av webbplatsen

5. **Konfigurera filter (valfritt):**
   - Inkludera endast vissa sökvägar (t.ex. `/docs/*`)
   - Exkludera specifika undersidor (t.ex. `/arkiv/*`)
   - Ange mönster för vilka delar av sidorna som ska ingå

6. **Ange crawling-frekvens (om tillgängligt):**
   - Engångs-crawling
   - Schemalagd återkommande (dagligen, veckovis, etc.)

7. **Starta crawling:** Initiera processen och övervaka förloppet.

8. **Granska resultat:** När processen är klar, kontrollera indexerad data och kvalitet.

!!! tip "Djup vs. Bredd"
    För teknisk dokumentation: Använd djupare crawling med färre utgångspunkter.
    
    För innehållsrika webbplatser: Använd grundare crawling med fler specifika utgångspunkter.

### Avancerade inställningar

För mer precis kontroll över crawling-processen kan du använda dessa inställningar:

- **Selektorer:** Ange CSS-selektorer för att markera endast specifika delar av en sida
- **Exkluderingsregler:** Undvik att crawla vissa domäner, undersidor eller filtyper
- **Autentisering:** Konfigurera inloggningsinformation för att komma åt skyddat innehåll
- **Rate-limiting:** Ställ in fördröjningar mellan förfrågningar för att minimera belastning på webbservrar

!!! warning "Etisk crawling"
    Se alltid till att respektera:
    
    1. **robots.txt-filer:** Dessa anger vilka delar av en webbplats som får crawlas
    2. **Rate-limits:** Överbelasta inte webbservrar med för många förfrågningar
    3. **Upphovsrätt:** Säkerställ att du har rätt att använda innehållet

## Dokumentbaserad kunskapsinhämtning

Förutom webbplatser kan Intric även extrahera och indexera information från uppladdade dokument:

- PDF-filer
- Word-dokument (.docx)
- Excel-filer (.xlsx)
- PowerPoint-presentationer (.pptx)
- Textfiler (.txt)
- CSV-filer
- JSON-filer

### Lägga till dokumentsamlingar

1. **Navigera till Kunskapskällor**
2. **Välj "Lägg till dokumentsamling"**
3. **Skapa eller välj en samling**
4. **Ladda upp dokument** till samlingen
5. **Konfigurera bearbetning** (chunking-storlek, överlappning)
6. **Starta indexeringen**

## Använda crawlade kunskapskällor med assistenter

När du har skapat en kunskapskälla genom crawling kan du koppla den till en eller flera assistenter:

1. **Gå till assistentinställningar:**
   - För en ny assistent: Under skapandeprocessen
   - För en befintlig: Via redigeringsläget

2. **Hitta sektionen "Knowledge"**

3. **Klicka på "Select additional knowledge sources"**

4. **Välj dina crawlade kunskapskällor** från listan

5. **Spara assistentinställningarna**

Assistenten kan nu använda den crawlade informationen för att besvara användarfrågor med [RAG-tekniken](vad-ar-rag.md).

!!! note "Förutsättningar"
    Se till att du har korrekta behörigheter för att läsa den data som ska crawlas.

!!! tip "Optimera crawling"
    Använd filter och metadatataggar för att begränsa vilka sektioner som indexeras.

## Felsökning och optimering

### Vanliga problem och lösningar

| Problem | Möjlig orsak | Lösning |
|:--------|:-------------|:--------|
| Innehåll saknas | Crawling-djupet för lågt | Öka antalet nivåer som crawlas |
| Irrelevant information | För brett crawling-scope | Använd mer specifika filter och selektorer |
| Långsam crawling | För många sidor | Begränsa omfattningen eller använd selektiv crawling |
| Blockeringar | För aggressiv crawling | Implementera fördröjningar mellan förfrågningar |
| Föråldrad information | Ingen omindexering | Schemalägg regelbundna uppdateringar |

### Optimera kvaliteten på crawlad data

För att få bästa möjliga resultat från crawlade kunskapskällor:

1. **Var specifik:** Crawla endast de delar av webbplatsen som innehåller relevant information
2. **Prioritera kvalitet:** Färre, mer relevanta sidor ger ofta bättre resultat än många irrelevanta
3. **Uppdatera regelbundet:** Schemalägg omindexering baserat på hur ofta innehållet ändras
4. **Testa med frågor:** Utvärdera kunskapsbasen genom att ställa typiska frågor till assistenten

## Relaterade ämnen

- [Vad är RAG?](vad-ar-rag.md)
- [Skapa och hantera assistenter](../assistenter/skapa-assistenter.md)
- [Hantera kunskapskällor](hantera-kunskapskallor.md)