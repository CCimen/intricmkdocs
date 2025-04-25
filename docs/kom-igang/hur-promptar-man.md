---
title: Hur promptar man effektivt?
---

# Hur promptar man effektivt?

En effektiv prompt kan jämföras med tydliga instruktioner till en kunnig medarbetare. Ju mer strukturerad och precis din prompt är, desto bättre blir AI-assistentens svar.

## De fem byggstenarna för effektiva prompts

<div class="grid cards" markdown>

-   :material-target:{ .lg .middle } **Mål**

    ---
    
    Vad vill du uppnå? Definiera tydligt vad du vill ha hjälp med.
    
    *"Sammanfatta rapporten..."*

-   :material-information-outline:{ .lg .middle } **Kontext**

    ---
    
    Bakgrundsinformation som hjälper assistenten förstå sammanhanget.
    
    *"...om kommunens vattenförsörjning från 2023..."*

-   :material-format-list-bulleted:{ .lg .middle } **Format**

    ---
    
    Specificera hur du vill att svaret ska presenteras.
    
    *"...i en punktlista med max 7 punkter..."*

-   :material-account-outline:{ .lg .middle } **Roll**

    ---
    
    Vilken synvinkel eller expertis vill du att assistenten ska utgå från?
    
    *"...som om du var en vattenresursexpert..."*

-   :material-cancel:{ .lg .middle } **Begränsning**

    ---
    
    Sätt gränser för svaret eller uppgiften.
    
    *"...använd enkelt språk och undvik tekniska termer."*

</div>

!!! tip "Kom ihåg"
    Du behöver inte använda alla fem byggstenar i varje prompt - anpassa efter ditt behov. För enklare frågor kan ibland bara mål och format räcka.

## Före och efter: Exempel på förbättrade prompts

=== "Otydlig prompt / Tydlig prompt"

    **Otydlig prompt**
    ```
    Förklara GDPR.
    ```
    
    **Tydlig prompt**
    ```
    Agera som dataskyddsjurist och förklara de viktigaste 
    principerna i GDPR för nyanställda inom offentlig sektor. 
    Använd max 150 ord och en punktlista. Fokusera särskilt 
    på vad som är viktigt att tänka på vid hantering av 
    personuppgifter i kommunala verksamheter.
    ```

=== "Medborgarservice"

    **Otydlig prompt**
    ```
    Svara på en fråga om bygglov.
    ```
    
    **Tydlig prompt**
    ```
    Du är kundtjänstmedarbetare på en kommunal bygglovsavdelning.
    Skriv ett vänligt och informativt svar till en medborgare som
    frågar: "Hur lång tid tar det att få bygglov för en tillbyggnad?"
    
    Svaret ska:
    1. Vara högst 150 ord
    2. Förklara den normala handläggningstiden
    3. Nämna vilka faktorer som kan påverka tidsåtgången
    4. Innehålla ett tips om vad personen kan göra för att
       processen ska gå smidigare
    ```

=== "Dokumentbearbetning"

    **Otydlig prompt**
    ```
    Sammanfatta detta dokument.
    ```
    
    **Tydlig prompt**
    ```
    Sammanfatta bifogad PDF (kommunens miljöstrategi) med fokus på
    konkreta åtgärder och mål. Strukturera sammanfattningen enligt följande:
    
    1. En inledande paragraf (max 50 ord) som beskriver dokumentets
       övergripande syfte
    2. 5-7 punkter med de viktigaste åtgärderna
    3. En tabell som visar miljömålen och när de ska vara uppnådda
    
    Använd ett tydligt och lättbegripligt språk anpassat för invånare
    utan expertkunskap inom miljöområdet.
    ```

## Praktiska promptningsmönster

Vissa typer av strukturer fungerar särskilt bra för specifika uppgifter:

### Stegvis resonemang

För komplexa frågor där svaret kräver flera tankeled:

```markdown
Tänk steg för steg för att lösa följande problem:
[Beskriv problemet]

1. Börja med att identifiera vilken information vi har
2. Bestäm vilken metod som är lämplig för att lösa problemet
3. Tillämpa metoden och visa dina beräkningar
4. Kontrollera om svaret är rimligt
5. Sammanfatta lösningen
```

### Format-mall

När ett specifikt format behövs:

```markdown
Skapa ett protokoll för kommunstyrelsemötet baserat på följande
anteckningar. Använd följande mall:

PROTOKOLL
Kommunstyrelsen, [Datum]
Plats: [Plats]

Närvarande: [Lista med namn]

§1. Mötets öppnande
[Text]

§2. Val av justerare
[Text]

...osv.
```

### Rollbaserad prompt

När du vill ha ett svar från ett specifikt perspektiv:

```markdown
Du är en erfaren stadsplanerare med 20 års erfarenhet av 
hållbar stadsutveckling i mindre kommuner. Analysera följande 
förslag till ny översiktsplan med fokus på möjligheter och
utmaningar för hållbara transporter.
```

![Prompt-exempel](../assets/images/prompt-exempel.png){ width="550" loading=lazy }

## Vanliga misstag att undvika

| Misstag | Problem | Förbättring |
|---------|---------|-------------|
| För vaga instruktioner | "Sammanfatta texten" ger oförutsägbara resultat | "Sammanfatta texten i 3 stycken med fokus på ekonomiska konsekvenser" |
| Otillräcklig kontext | "Vad tycker du om förslaget?" (utan att förklara vilket förslag) | "Nedan finns kommunens förslag till ny parkeringspolicy. Vilka för- och nackdelar ser du med denna?" |
| Motstridiga instruktioner | "Skriv en detaljerad analys men gör den mycket kort" | Bestäm dig för antingen detaljrikedom eller korthet |
| För många krav på en gång | Olika format, perspektiv och krav i samma prompt | Dela upp komplexa uppgifter i flera enklare prompts |

!!! warning "Var uppmärksam på 'promptinjektioner'"
    Undvik att inkludera användarindata direkt i prompten utan kontroll, då det kan leda till att AI-assistenten följer oönskade instruktioner från tredje part istället för dina.

## Avancerade promptningstekniker

### Chain-of-Thought (Tankekedja)

För komplexa uppgifter, be assistenten att "tänka högt" steg för steg:

```markdown
Analysera bifogat budgetförslag för IT-avdelningen och identifiera
potentiella besparingar. Tänk steg för steg:
1. Gå igenom budgetposterna en i taget
2. Jämför med föregående års kostnader
3. Identifiera ovanligt höga kostnadsökningar
4. Föreslå alternativa lösningar eller effektiviseringar
```

### Few-shot learning (Inlärning med exempel)

Ge exempel på vad du förväntar dig:

```markdown
Förenkla följande myndighetstexter till klarspråk. Behåll all
väsentlig information men gör språket tillgängligt för alla.

Exempel:
Original: "Vidare åläggs fastighetsinnehavaren att ombesörja 
bortforslande av avfall enligt renhållningsförordningen."
Förenkling: "Du som äger fastigheten ansvarar också för att avfall
tas om hand enligt reglerna om sophantering."

Texter att förenkla:
1. [Första texten]
2. [Andra texten]
```

### Självkritik och revidering

Be assistenten utvärdera sitt eget arbete och göra förbättringar:

```markdown
Skriv ett utkast till ett pressmeddelande om kommunens nya 
kulturhus. När du är klar, granska texten kritiskt och föreslå
förbättringar. Revidera sedan texten baserat på din kritik.
```

---

### Relaterade ämnen
- [Vad är en prompt?](vad-ar-en-prompt.md)
- [Skapa assistenter](../assistenter/skapa-assistenter.md)
- [Anpassa systemprompt](../assistenter/anpassa-systemprompt.md)
