---
title: Vad är en prompt?
---

# Vad är en prompt?

En **prompt** är den instruktion eller fråga du ger till en AI-assistent. Precis som när du ger instruktioner till en kollega, påverkar promptens tydlighet och precision kvaliteten på svaret du får.

![Prompt-fältet](../assets/images/prompt-field.png){ width="550" loading=lazy }

## Promptens byggstenar

En effektiv prompt bygger vanligtvis på fem viktiga element som hjälper AI-assistenten att förstå exakt vad du behöver:

<div class="grid cards" markdown>

-   :material-target:{ .lg .middle } **Mål**

    ---
    
    Vad vill du uppnå? Var specifik med vad du vill att assistenten ska göra.
    
    *"Sammanfatta huvudpunkterna i detta dokument..."*

-   :material-information-outline:{ .lg .middle } **Kontext**

    ---
    
    Relevant bakgrundsinformation som hjälper assistenten förstå uppgiften.
    
    *"...för en presentation till kommunstyrelsen som inte är insatt i detaljerna..."*

-   :material-format-list-bulleted:{ .lg .middle } **Format**

    ---
    
    Hur vill du ha svaret strukturerat? Specificera önskat format.
    
    *"...i form av 5-7 punkter med en kort rubrik för varje punkt..."*

-   :material-account-outline:{ .lg .middle } **Roll**

    ---
    
    Vilken expertkompetens eller perspektiv vill du att assistenten ska anta?
    
    *"...ur ett ekonomiskt perspektiv..."*

-   :material-cancel:{ .lg .middle } **Begränsning**

    ---
    
    Definiera ramar och begränsningar för uppgiften.
    
    *"...använd enbart information från dokumentet, utan att lägga till egna tolkningar."*

</div>

!!! tip "Du behöver inte använda alla element varje gång"
    Anpassa din prompt efter situationen. För enkla frågor kan en kort mening räcka, medan mer komplexa uppgifter kan kräva samtliga byggstenar.

## Exempel på effektiva prompts

=== "Dokumentsammanfattning"
    ```markdown
    Sammanfatta bifogad PDF om kommunens nya avfallshanteringsplan.
    Fokusera på de delar som påverkar invånarna direkt.
    Formatera svaret som max 10 numrerade punkter följt av en
    kort sammanfattning på 2-3 meningar som kan användas i ett
    pressmeddelande.
    ```

=== "Mötesanteckningar"
    ```markdown
    Du är sekreterare vid ett möte om budgetplanering. 
    Transkribera bifogad ljudfil och skapa strukturerade 
    mötesanteckningar med följande delar:
    1. Deltagare
    2. Huvudfrågor som diskuteras
    3. Beslut som fattas
    4. Åtgärdspunkter med ansvariga personer
    
    Markera viktiga datum med fetstil.
    ```

=== "Textförbättring"
    ```markdown
    Förbättra språket i följande text från vår hemsida så att den
    blir mer lättläst och tillgänglig för personer med begränsade
    svenskkunskaper. Behåll all information men förenkla meningsbyggnad
    och ordval. Texten ska vara vänlig och inkluderande:
    
    [Klistra in text här]
    ```

=== "Idégenerering"
    ```markdown
    Agera som innovationsexpert. Generera 7 kreativa idéer för hur
    vår kommun kan använda digital teknik för att förbättra äldres
    delaktighet i samhällslivet. För varje idé, beskriv:
    - Grundkoncept (1 mening)
    - Potentiella fördelar (2-3 punkter)
    - Utmaningar att ta hänsyn till (1-2 punkter)
    ```

## Praktiska tillämpningar i offentlig sektor

AI-assistenter kan hjälpa till med många olika arbetsuppgifter inom offentlig sektor:

| Område | Användningsområde | Exempel på prompt |
|--------|-------------------|------------------|
| **Administration** | Sammanfatta dokument | "Sammanfatta huvudpunkterna i bifogad rapport om vattenförsörjningen i kommundelarna X, Y och Z." |
| **Medborgarservice** | Svara på vanliga frågor | "Skriv ett vänligt och informativt svar till en medborgare som undrar över processen för bygglovsansökan." |
| **Möteshantering** | Protokollskrivning | "Omvandla anteckningarna nedan till ett formellt mötesprotokoll enligt kommunens mall." |
| **Kommunikation** | Textanpassning | "Omformulera denna tekniska beskrivning till en lättförståelig text för kommunens nyhetsbrev." |
| **Planering** | Checklistor | "Skapa en detaljerad checklista för arrangemang av ett offentligt samråd om den nya översiktsplanen." |

!!! warning "Viktigt att tänka på"
    Var alltid noga med att granska AI-genererade texter innan de används i officiella sammanhang. AI-assistenten är ett verktyg för att effektivisera arbetet, inte ersätta mänskligt omdöme.

## Exempel på en komplett prompt

```markdown
Du är kommunikationsexpert inom offentlig förvaltning.
Omformulera följande text från vårt reglemente så att den blir
lättbegriplig för en person med grundskoleutbildning, men utan
att förlora någon väsentlig information eller juridisk innebörd.

Använd korta meningar, aktiv form och vardagligt språk.
Strukturera texten med tydliga rubriker och punktlistor där det
passar. Lägg särskild vikt vid att förklara facktermer inom
parentes.

Text att omformulera:
[Klistra in text här]
```

---

### Nästa steg
- [Hur promptar man effektivt?](hur-promptar-man.md)
- [Skapa assistenter](../assistenter/skapa-assistenter.md)
- [Anpassa systemprompt](../assistenter/anpassa-systemprompt.md)