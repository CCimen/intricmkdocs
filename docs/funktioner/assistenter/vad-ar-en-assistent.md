---
title: Vad är en assistent?
---

# Vad är en assistent?

En **assistent** i Intric är en _förkonfigurerad_ AI-chatbot som redan vet:

1. **Vem den ska vara** – definieras genom en **systemprompt**  
2. **Vilken motor den ska använda** – valet av en **AI-modell**  
3. **Vilken fakta den får stöd av** – via **bilagor** eller en **kunskaps­bas** (RAG)

Genom att använda en assistent slipper du upprepa samma instruktioner varje gång, vilket garanterar konsekventa och effektiva svar.

---

## Vad kan en assistent göra?

<div class="grid cards" markdown>
- :material-note-text-multiple-outline:{ .md-icon .lg } **Sammanfatta**  
  Dra in ett dokument och få en punktlista på sekunder.
- :material-message-question-outline:{ .md-icon .lg } **Besvara FAQ**  
  Hämta svar direkt från interna policydokument – dygnet runt.
- :material-lightbulb-outline:{ .md-icon .lg } **Brainstorma**  
  Generera kreativa idéer för kampanjer eller möten.
</div>

---

## Huvudkomponenter

### 1. Systemprompt *(Roll & Regler)*

!!! info "Vad är en systemprompt?"
    Det är assistentens **regelbok**. Du definierar vilken roll den ska ha, vad den får säga och vilka begränsningar som gäller.  
    **Exempel:**

    ```markdown
    Du är HR-expert och svarar på frågor om semester.  
    - Tonen ska vara vänlig men formell  
    - Om du är osäker, hänvisa till hr@företag.se
    ```

### 2. AI-modell *(Motor)*

Välj en modell som motsvarar dina behov. Exempel:

| Modelltyp           | Passar bäst för         | Kommentar                |
|---------------------|-------------------------|--------------------------|
| **Allmän LLM**      | Vanlig textgenerering   | T.ex. GPT-4, ChatGPT      |
| **Kodspecificerad** | Kodgranskning, felsökning | Ex. Code Llama           |
| **Domäntränad**     | Nischad domänkunskap    | Kräver egen hostning     |

!!! tip
    För de flesta är standardmodellen ett bra utgångsläge. Byt ut om du behöver snabbare, mer kostnadseffektiva eller mer domänanpassade svar.

### 3. Datakällor *(Fakta)*

Datakällan kan levereras på två huvudsakliga sätt:

|                        | **Bilagor**             | **Kunskaps­källor (RAG)**          |
|------------------------|:-----------------------:|:---------------------------------:|
| **Hur skickas data?**  | Alltid med varje prompt | Hämtas "on-demand" via crawling   |
| **Volym**              | Upp till ≈ 50 sidor      | Kan omfatta hundratusentals sidor |
| **Kostnad**            | Hög tokenanvändning      | Lägre tack vare cachelagring      |
| **Uppdatering**        | Uppdateras manuellt      | Uppdateras automatiskt enligt schema |

!!! note "När ska du välja vad?"
    *Bilagor* fungerar bäst för korta policies eller mallar som **alltid** behövs, medan *kunskaps­källor* (RAG) är optimala för stora eller kontinuerligt uppdaterade datamängder.

---

## AI-inställningar (Finjustering)

| Inställning         | Funktion                                            | Rekommendation                            |
|---------------------|-----------------------------------------------------|-------------------------------------------|
| **Temperature**     | 0 = mycket faktabaserat, 1 = mycket kreativt        | 0.2–0.4 för support/svar, 0.7+ för idéer    |
| **Model behavior**  | Exempel: _Default_, _Creative_, _Deterministic_      | Anpassa efter uppgiftens krav             |
| **Max tokens**      | Bestämmer hur långt svaret får bli                  | Sätt en gräns för att undvika höga kostnader|

---

## Insights (valfritt)

!!! warning "Datainsamling"
    Om du aktiverar loggning av frågor och svar får du insikter i:
    - Vilka ämnen som är mest populära  
    - Kvaliteten på svaren  
    - Eventuella luckor i din kunskaps­bas  

    **Notera:** Användare bör informeras att konversationer sparas om denna funktion aktiveras.

---

## Skapa din egen assistent – på 30 sekunder

1. Gå till **Assistenter → Skapa assistent**.
2. Namnge din assistent och skriv in en **systemprompt**.
3. Välj önskad **AI-modell**.
4. Lägg till en **bilaga** eller **kunskaps­källa** (om det behövs).
5. Klicka på **Spara** – så är din assistent klar!

---

## Vanliga frågor

| Fråga                          | Kort svar                                  |
|--------------------------------|--------------------------------------------|
| _Kan jag kopiera en assistent?_    | Ja, välj **Duplicera** i listan.             |
| _Kan jag byta modell i efterhand?_  | Öppna assistenten och gå till **AI-inställningar**. |
| _Hur delar jag med teamet?_         | Skapa eller flytta assistenten till ett **Space**.  |

---

### Nästa steg

- [Skapa assistenter – steg för steg](skapa-assistenter.md)  
- [Hur promptar man effektivt?](../../kom-igang/hur-promptar-man.md)  
- [Vad är RAG?](../kunskapsbaser/vad-ar-rag.md)  
- [Vad är crawling?](../kunskapsbaser/vad-ar-crawling.md)