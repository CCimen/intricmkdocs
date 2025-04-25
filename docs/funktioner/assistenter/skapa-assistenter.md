---
title: Skapa och hantera assistenter
---

# Skapa och hantera assistenter

En **assistent** är en chat-bot du skräddarsyr med regler, modellval och – om du vill – en egen kunskapsbas.

<div class="grid cards" markdown>
- :material-rocket-launch-outline:{ .md-icon .lg } **Snabbstart**  
  [Tre-minutersguiden »](#tre-minutersguiden)
- :material-school-outline:{ .md-icon .lg } **Lär dig mer**  
  Läs hela guiden nedan.
</div>

---

## Tre-minutersguiden  <a id="tre-minutersguiden"></a>

!!! example "Skapa en assistent i Intric"
    ![Create-modal](../assets/images/create-assistant-modal.png){ width="450" }

    1. **Assistenter** → **Skapa assistent**  
    2. Döp den – ex. *Mötes­samman­fattare*  
    3. Klicka **Skapa assistent** → redigeraren öppnas

> :material-check-circle-outline:{ .md-icon } *Klart!* Testa direkt i chatten.

---

## Detaljerade inställningar

=== "1. Allmänt"
    **Namn och beskrivning**

    | Fält | Tips |
    |------|------|
    | **Namn** | Kort, sökbart (ex. “HR-FAQ-bot”) |
    | **Beskrivning** | 1–2 meningar om uppgiften |

=== "2. Systemprompt"
    ```markdown title="Exempel – Kundtjänst"
    Du är kundtjänst för Sundsvalls kommun.  
    - Var artig & kortfattad  
    - Okunskap? → 060-19 10 00  
    - Avsluta med “Kan jag hjälpa dig mer?”
    ```

=== "3. Bilagor"
    Bilagor skickas **alltid** med varje prompt.

    <details>
    <summary>🗂 Lägg till eller ta bort</summary>

    1. *Attachments* → **Upload attachment**  
    2. Välj fil → vänta tills status = *Done*  
    3. Ta bort? Klicka :material-delete:.

    !!! warning "Token-gräns"
        Stora bilagor = högre kostnad & risk att äldre meddelanden kapas.
    </details>

=== "4. Kunskapskällor (RAG)"
    ![Dropdown](../assets/images/knowledge-dropdown.png){ width="320" }

    | Typ | Använd när | Guide |
    |-----|------------|-------|
    | **Collection** | Du har filer | [Se filuppladdning »](#ladda-upp-filer) |
    | **Website** | Info finns online | [Se crawling-exempel »](../kunskapsbaser/vad-ar-crawling.md#praktiskt-exempel--webbplats) |

=== "5. AI-inställningar"

    | Parameter | Beskrivning | Rek. |
    |-----------|-------------|------|
    | **Model** | GPT-4o, Claude 3 etc. | Börja med standard |
    | **Temperature** | 0 = fakta, 1 = kreativt | 0.2–0.4 för support |
    | **Model behavior** | *Creative*, *Deterministic*… | Välj efter uppgift |

=== "6. Insights"
    !!! tip "När ska du slå på?"
        Aktivera när du vill se vilka frågor som återkommer eller mäta nyttan.

---

## Vanliga uppgifter

=== "Byt namn"
    1. Listan **Assistenter**  
    2. :material-dots-horizontal: → **Redigera**  
    3. Ändra namn → **Spara**

=== "Duplicera"
    1. :material-dots-horizontal: → **Duplicera**  
    2. Redigera kopian

=== "Dela med Space"
    1. Skapa (eller klona) assistenten **inne i** Spacet  
    2. Lägg till samma prompt & källor

---

## FAQ

| Fråga | Svar kort |
|-------|-----------|
| **Kan jag återställa äldre version?** | Ja, se fliken *Versions* i redigeraren. |
| **Hur tar jag bort en assistent?** | :material-delete: → **Delete** i listan. |
| **Stöd för röst?** | Ja, bocka i *Enable audio* i *Chat settings*. |

---

### Relaterade ämnen
- [Vad är en assistent?](vad-ar-en-assistent.md)
- [Vad är RAG?](../kunskapsbaser/vad-ar-rag.md)
- [Skillnad personlig yta / Space](skillnad-personlig-vs-space.md)
