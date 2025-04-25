---
title: Skapa och hantera assistenter
---

# Skapa och hantera assistenter

Att skapa en AI-assistent i Intric är en central funktion som låter dig anpassa AI-modeller för specifika uppgifter och arbetsflöden. En assistent kombinerar en AI-modell med specifika instruktioner (en systemprompt) och eventuellt en kopplad kunskapsbas.

## Skapa en ny assistent

### Steg-för-steg guide:

1. **Navigera till Assistenter:** Logga in i Intric och välj "Assistenter" i huvudmenyn.
2. **Klicka på "Skapa Assistent":** Fyll i detaljer för den nya assistenten.
3. **Namnge Assistenten:** Ge ett beskrivande namn, t.ex. "Sammanfattare av mötesanteckningar".
4. **Skriv en Systemprompt:** Definiera assistentens roll och beteende.
5. **Välj AI-modell:** Välj en språkmodell som passar ditt behov.
6. **Koppla Kunskapsbas (valfritt):** Koppla interna data som assistenten kan hämta information från.
7. **Avancerade Inställningar (valfritt):** Justera temperatur, max tokens etc.
8. **Spara Assistenten:** Klicka på "Spara" eller "Skapa".

!!! success "Assistenten är skapad!"
    Din nya assistent finns nu tillgänglig i listan och är redo att användas.

## Konfigurera assistentinställningar

När du skapar eller redigerar en assistent har du tillgång till flera inställningar. Här är en detaljerad förklaring av varje sektion:

### Allmänna inställningar

#### Namn och beskrivning

- **Namn:** Detta är assistentens identifikator som visas i listor och sökning. Ett bra namn är:
  - Kort och beskrivande
  - Indikerar assistentens syfte
  - Lätt att hitta i en lista

- **Beskrivning:** En kort introduktion som visas för användare som interagerar med assistenten. Beskrivningen bör förklara:
  - Assistentens huvudsyfte
  - Vilka typer av frågor den är bäst på att svara på
  - Eventuella särskilda instruktioner för användning

!!! tip "Byta namn på en assistent"
    För att **byta namn på en existerande assistent**:
    
    1. Gå till assistentlistan
    2. Klicka på menyn (tre punkter) bredvid assistenten
    3. Välj "Redigera"
    4. Uppdatera namnfältet
    5. Spara ändringarna

#### Prompt (Instruktioner)

Promptfältet innehåller de grundläggande instruktioner som styr assistentens beteende och svarsstil. Detta är det vi kallar "systemprompt".[^1]

[^1]: Systemprompt skickas till AI-modellen i början av varje konversation, innan användarens första fråga.

En effektiv prompt bör innehålla:

- **Roll och identitet:** Vem eller vad assistenten ska vara
- **Expertisområden:** Vilka ämnen assistenten ska fokusera på
- **Tonstil:** Formell, informell, teknisk, enkel, etc.
- **Svarslängd:** Kortfattad eller detaljerad
- **Begränsningar:** Vad assistenten inte ska göra eller diskutera
- **Formatregler:** Hur svar ska struktureras

```markdown title="Exempel på en prompt för en kundserviceassistent"
Du är en kundserviceassistent för Sundsvalls kommun som hjälper invånare med frågor om kommunala tjänster.

Följ dessa riktlinjer:
- Var alltid artig och professionell
- Ge korta, koncisa svar när det är möjligt
- När du inte vet svaret, hänvisa till kommunens kundtjänst på 060-19 10 00
- Svara bara på frågor relaterade till kommunens verksamhet
- Avsluta svaret med en fråga om det finns något mer du kan hjälpa till med
```

### Bilagor och kunskapskällor

#### Hantera bilagor (Attachments)

Bilagor är dokument som alltid skickas till AI-modellen med varje prompt.

**Så här lägger du till en bilaga:**

1. Under sektionen "Attachments", klicka på "Upload attachment"
2. Välj filen från din dator
3. Vänta på att uppladdningen slutförs
4. Filen visas nu i listan över bilagor

**Så här tar du bort en bilaga:**

1. Hitta bilagan i listan
2. Klicka på papperskorgsikonen bredvid bilagan
3. Bekräfta borttagningen

!!! warning "Filstorlek och tokenanvändning"
    Bilagor räknas med i den totala tokengränsen för varje konversation. Stora filer kan leda till att gränsen nås snabbare och att äldre meddelanden i konversationen trimmas bort.

#### Hantera kunskapskällor (Knowledge)

Kunskapskällor är externa informationskällor som assistenten kan söka i efter relevant information vid behov.

**Så här lägger du till en kunskapskälla:**

1. Under sektionen "Knowledge", klicka på "Select additional knowledge sources"
2. Välj källtyp:
   - **Collections:** Mappar med dokument (PDF, CSV, TXT, etc.)
   - **Websites:** Crawlade webbplatser

3. För Collections:
   - Välj en befintlig samling eller skapa en ny
   - Ladda upp filer till samlingen

4. För Websites:
   - Ange URL:en som ska crawlas
   - Konfigurera crawling-inställningar (djup, omfattning)
   - Starta crawling-processen (mer om detta i [Vad är crawling?](../kunskapsbaser/vad-ar-crawling.md))

**Så här tar du bort en kunskapskälla:**

1. Hitta kunskapskällan i listan
2. Klicka på kryssikonen bredvid källan
3. Bekräfta borttagningen

!!! tip "Kombinera kunskapskällor"
    Du kan lägga till flera olika kunskapskällor till samma assistent för att skapa en bredare kunskapsbas.

### AI-inställningar

#### Completion model

Completion model är den AI-modell som används för att generera svar på användarens frågor.

**Så här väljer du en lämplig modell:**

1. Klicka på rullgardinsmenyn under "Completion model"
2. Välj bland tillgängliga modeller baserat på:
   - **Prestanda:** Mer avancerade modeller ger ofta bättre svar men kan vara långsammare
   - **Kapacitet:** Större modeller kan hantera mer komplexa uppgifter
   - **Specialisering:** Vissa modeller är bättre på kod, andra på generell text
   - **Säkerhetsnivå:** Olika modeller har olika säkerhetsprofiler
   - **Kostnad:** Mer avancerade modeller kostar ofta mer att använda

!!! info "Tillgängliga modeller"
    Vilka modeller som är tillgängliga beror på din organisations konfiguration och vilka modellintegreringar som har aktiverats i Intric.

#### Model behavior

Model behavior styr hur AI-modellen genererar svar. Du kan välja bland olika förinställningar:

- **Default:** Balanserad mellan kreativitet och konsekvens
- **Creative:** Mer varierade och kreativa svar, bra för brainstorming
- **Deterministic:** Mer konsekventa svar, idealisk för procedurella uppgifter
- **Custom:** Anpassade parametrar för specifika behov

**Temperatur**

Den viktigaste parametern är Temperature, som styr slumpmässigheten i svaren:

- **0:** Helt deterministisk - samma fråga ger alltid (nästan) samma svar
- **0.5:** Måttlig variation - balanserad mellan konsekvens och kreativitet
- **1.0:** Standard - mer variation i svaren
- **1.5:** Hög kreativitet - betydande variation
- **2.0:** Maximal kreativitet - mest oförutsägbara svar

Välj en låg temperatur (0-0.3) för:
- Faktabaserade svar
- Steg-för-steg instruktioner
- Konsekvent innehåll

Välj en hög temperatur (0.7-2.0) för:
- Kreativt skrivande
- Idégenerering
- Varierande svar

#### Insights

Insights-funktionen samlar data om assistentanvändning för administratörer.

**När aktiverad kan administratörer se:**
- Vilka frågor som ställts (konversationshistorik)
- Användningsfrekvens
- Populära ämnen
- Prestanda och svarstider

**Integritetshänsyn:**

!!! warning "Datainsamling"
    När insights är aktiverad sparas all konversationsdata och kan ses av administratörer. Informera användare om detta när det är relevant.

Aktivera insights när:
- Du vill förbättra assistenten baserat på verkliga användningsmönster
- Du behöver övervaka användning för kvalitets- eller efterlevnadssyften
- Du vill identifiera gemensamma frågor för att förbättra kunskapsbasen

## Vanliga frågor

### Hur ändrar jag en befintlig assistent?

1. Gå till assistentlistan
2. Klicka på menyn (tre punkter) bredvid assistenten
3. Välj "Redigera"
4. Gör dina ändringar
5. Klicka på "Spara"

### Kan jag kopiera en assistent?

Ja, du kan duplicera en assistent för att använda den som utgångspunkt för en ny:

1. Gå till assistentlistan
2. Klicka på menyn (tre punkter) bredvid assistenten
3. Välj "Duplicera"
4. En kopia skapas med namnet "Kopia av [ursprungligt namn]"
5. Redigera den nya kopian efter behov

### Kan jag dela min assistent med andra?

Ja, assistenter kan delas beroende på var de skapas:

- **Personliga assistenter:** Kan endast användas av dig
- **Space-assistenter:** Kan användas av alla medlemmar i Space:et enligt deras behörighetsnivå

För att flytta en assistent från din personliga yta till ett Space:
1. Skapa en ny assistent i Space:et
2. Kopiera över inställningarna från din personliga assistent
3. Lägg till relevanta kunskapskällor och bilagor på nytt

## Relaterade ämnen

- [Vad är en assistent?](vad-ar-en-assistent.md)
- [Skillnad mellan personlig yta och Space](skillnad-personlig-vs-space.md)
- [Vad är RAG?](../kunskapsbaser/vad-ar-rag.md)
- [Vad är crawling?](../kunskapsbaser/vad-ar-crawling.md)