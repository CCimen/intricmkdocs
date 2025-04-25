---
title: Vad är en assistent?
---

# Vad är en assistent?

En **AI-assistent** i Intric är en chat-baserad agent som använder en språkmodell för att utföra specifika uppgifter utifrån dina instruktioner. Assistenter kombinerar:

- **Systemprompt:** Grundläggande instruktioner som definierar assistentens roll och beteende.  
- **AI-modell:** Det underliggande språksystemet som genererar svar.  
- **Kunskapsbas (valfritt):** Extern information som assistenten kan hämta data från för mer relevanta och korrekta svar.  

Med en AI-assistent kan du:
- Automatisera repetitiva textuppgifter  
- Sammanfatta eller analysera dokument  
- Skapa anpassade arbetsflöden för olika användarbehov

## Viktiga komponenter i en assistent

En Intric-assistent består av flera komponenter som du kan anpassa för att skapa den perfekta AI-lösningen för dina behov:

### Allmänna inställningar

!!! info "Allmänna inställningar"
    Dessa inställningar definierar assistentens grundläggande identitet och beteende.

#### Namn och beskrivning

**Namn** är det som visas för användarna och bör tydligt indikera assistentens syfte eller roll.

**Beskrivning** är en kort introduktion som visas när en användare startar en ny session med assistenten. En bra beskrivning förklarar:
- Vad assistenten är designad att hjälpa med
- Eventuella begränsningar i dess kunskap eller kapacitet
- Hur användaren bäst interagerar med den

#### Prompt (Instruktioner)

**Prompt** är de grundläggande instruktioner som styr assistentens beteende och svarsstil. Detta är vad som kallas "systemprompt" och skickas till AI-modellen innan varje konversation.[^1]

[^1]: Till skillnad från användarens frågor, är systemprompt en dold instruktion som alltid finns med i bakgrunden och styr assistentens grundläggande beteende.

!!! tip "Promptoptimering"
    En välskriven prompt är nyckeln till en effektiv assistent. Se [Hur promptar man effektivt?](../../kom-igang/hur-promptar-man.md) för tips om hur du skapar bättre instruktioner.

### Bilagor och kunskapskällor

För att göra din assistent verkligt användbar kan du utöka dess förmågor med externa resurser:

#### Attachments (Bilagor)

**Attachments** är filer som alltid skickas med till AI-modellen i varje konversation. Detta är användbart för:

- Mallar som assistenten ska följa
- Referensdokument som innehåller viktiga riktlinjer
- Strukturerade data som assistenten alltid ska ha tillgång till

Bilagor skickas direkt till AI-modellen i varje prompt, vilket gör dem ideala för information som alltid behövs, men kan öka token-användningen.

#### Knowledge (Kunskapskällor)

**Knowledge** är externa informationskällor som assistenten kan söka i efter relevant information vid behov. Till skillnad från bilagor hämtas denna information dynamiskt genom [RAG-teknik](../kunskapsbaser/vad-ar-rag.md).

Kunskapskällor kan vara:
- **Collections:** Mappar med dokument (PDF, CSV, TXT, etc.)
- **Websites:** Crawlade webbplatser med nyttig information

!!! info "Knowledge vs. Attachments"
    **Knowledge** används för omfattande information som endast behövs ibland och hämtas selektivt med RAG-teknik.
    
    **Attachments** skickas alltid med varje prompt och är lämpliga för kortare, kritisk information som alltid behövs.

### AI-inställningar

AI-inställningar styr hur den underliggande språkmodellen fungerar:

#### Completion model

**Completion model** är den AI-modell som används för att bearbeta assistentens input och generera svar. Olika modeller har olika förmågor, styrkor och begränsningar gällande:

- Språkförmåga och kvalitet
- Kunskap (träningsdata)
- Specialiseringar (kod, text, kalkylark, etc.)
- Säkerhet och pålitlighet

#### Model behavior

**Model behavior** kontrollerar hur modellen genererar svar genom inställningar som:

- **Default:** Balanserad mellan kreativitet och konsekvens
- **Creative:** Mer varierade och kreativa svar, bra för brainstorming
- **Deterministic:** Mer konsekventa svar, idealisk för procedurella uppgifter
- **Custom:** Anpassade parametrar för specifika behov

Den viktigaste parametern inom model behavior är **temperature** som reglerar slumpmässighet:
- **Låg (0):** Mer deterministiska, fokuserade och konsekventa svar
- **Hög (2):** Mer kreativa, varierade och oförutsägbara svar

### Publikationsinställningar

#### Insights

**Insights** är en administratörsfunktion som samlar in användningsdata om assistenten. När aktiverad kan Space-administratörer och redaktörer se:

- Vilka frågor som ställts till assistenten
- Hur ofta assistenten används
- Användningsmönster över tid

Detta är värdefullt för att förbättra assistenten baserat på verklig användning.

## Nästa steg

För att lära dig mer om hur du arbetar med assistenter, utforska dessa resurser:

- [Hur skapar man assistenter?](skapa-assistenter.md)
- [Skillnad mellan personlig yta och Space](skillnad-personlig-vs-space.md)
- [Vad är RAG?](../kunskapsbaser/vad-ar-rag.md)
- [Vad är crawling?](../kunskapsbaser/vad-ar-crawling.md)