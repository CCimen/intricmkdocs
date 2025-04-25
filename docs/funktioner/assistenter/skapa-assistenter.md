---
title: Skapa och hantera assistenter
---

# Skapa och hantera assistenter

En **assistent** är en AI-chatbot du skräddarsyr med specifika instruktioner, modellval och – om du vill – en egen kunskapsbas för bättre svar inom ditt verksamhetsområde.

<div class="grid cards" markdown>
- :material-rocket-launch-outline:{ .md-icon .lg } **Snabbstart**  
  [Tre-minutersguiden för att komma igång »](#tre-minutersguiden)
- :material-school-outline:{ .md-icon .lg } **Lär dig mer**  
  [Utforska alla inställningar och möjligheter »](#detaljerade-installningar)
</div>

---

## Tre-minutersguiden {#tre-minutersguiden}

!!! tip "Kom igång på tre minuter"
    1. Klicka på **Assistenter** i huvudmenyn
    2. Välj **Skapa assistent**
    3. Ge assistenten ett beskrivande namn
    4. Klicka på **Skapa assistent**
    5. Testa din assistent direkt i chatten!

![Create-modal](../assets/images/create-assistant-modal.png){ align=center width="550" .shadow }

> :material-lightbulb-outline:{ .md-icon } **Tips:** Din nya assistent är nu redo att användas, men för att anpassa den behöver du gå vidare till redigeraren för att justera systemprompt och andra inställningar.

---

## Detaljerade inställningar {#detaljerade-installningar}

=== "1. Allmänt"
    **Namn och beskrivning** är de första uppgifterna du fyller i. Dessa hjälper både dig och andra användare att förstå vad assistenten är till för.

    | Fält | Beskrivning | Tips |
    |------|-------------|------|
    | **Namn** | Assistentens titel | Välj ett kort, beskrivande namn som är sökbart (t.ex. "HR-FAQ-bot", "Mötessammanfattare") |
    | **Beskrivning** | Kort introduktion | Skriv 1-2 meningar som tydligt beskriver assistentens syfte och användningsområde |

    ![Allmänna inställningar](../assets/images/create-assistant-modal.png){ align=right width="300" .shadow }

    !!! note "Tänk på"
        En bra beskrivning hjälper användare att förstå hur assistenten kan hjälpa dem och i vilka situationer den bör användas.

=== "2. Systemprompt"
    **Systemprompt** är de grundläggande instruktioner du ger till AI-modellen om hur assistenten ska bete sig, vilken ton den ska ha, och vilka uppgifter den ska utföra.

    ```markdown title="Exempel - Kundtjänstassistent"
    Du är kundtjänst för Sundsvalls kommun.
    
    Följ dessa riktlinjer i alla dina svar:
    - Var artig och kortfattad
    - Använd ett tydligt och enkelt språk
    - Om du inte kan svara på en fråga, hänvisa till kundtjänst på 060-19 10 00
    - Avsluta alltid med "Kan jag hjälpa dig med något mer?"
    ```

    !!! tip "Rekommendation för bättre systemprompt"
        * Definiera assistentens roll och identitet tydligt
        * Använd punktlistor för tydliga instruktioner
        * Specificera ton och samtalsstil
        * Inkludera riktlinjer för hur assistenten ska hantera frågor den inte kan besvara

=== "3. Bilagor"
    **Bilagor** (Attachments) är dokument som alltid skickas med varje prompt när någon chattar med assistenten. Detta är användbart för att ge assistenten tillgång till specifik information.

    <div class="grid" markdown>
    <div markdown>
    **Så här lägger du till bilagor:**
    
    1. Gå till fliken *Attachments*
    2. Klicka på **Upload attachment**
    3. Välj fil från din dator
    4. Vänta tills statusen visar *Done*
    
    **Ta bort en bilaga:**
    * Klicka på :material-delete: ikonen bredvid bilagan
    </div>
    <div markdown>
    ![Bilagor](../assets/images/knowledge-dropdown.png){ width="320" .shadow }
    </div>
    </div>

    !!! warning "Tänk på token-gränsen"
        Stora bilagor kan leda till högre kostnad och risk att äldre meddelanden i chatten kapas eftersom AI-modeller har en maxgräns för antal tokens de kan hantera per samtal.

=== "4. Kunskapskällor (RAG)"
    **Kunskapskällor** låter din assistent söka i specificerade databaser för att ge mer precisa och uppdaterade svar.

    ![Kunskapskällor](../assets/images/knowledge-dropdown.png){ align=right width="320" .shadow }

    | Typ | Beskrivning | Använd när | Guide |
    |-----|------------|------------|-------|
    | **Collection** | Samling av dokument | Du har specifika filer (PDF, Word, etc.) med viktig information | [Se filuppladdning »](#ladda-upp-filer) |
    | **Website** | Webbplatsinnehåll | Information finns på en webbplats eller intranät | [Se crawling-exempel »](../kunskapsbaser/vad-ar-crawling.md#praktiskt-exempel--webbplats) |

    !!! info "Vad är RAG?"
        RAG (Retrieval Augmented Generation) låter AI-modellen hämta relevant information från din databas innan den besvarar frågor, vilket ger mer korrekta och uppdaterade svar. [Läs mer om RAG »](../kunskapsbaser/vad-ar-rag.md)

=== "5. AI-inställningar"
    **AI-inställningar** låter dig finjustera hur assistenten genererar svar.

    | Parameter | Beskrivning | Rekommendation |
    |-----------|-------------|----------------|
    | **Model** | Vilken AI-modell som används (t.ex. GPT-4o, Claude 3) | Börja med standardmodellen och byt om du behöver specialfunktioner |
    | **Temperature** | Kontrollerar kreativitet vs konsekvens (0-1) | 0.2-0.4 för faktabaserade svar, 0.7-0.9 för kreativa uppgifter |
    | **Model behavior** | Fördefinierade beteendeprofiler | Välj utifrån användningsområde: *Creative*, *Deterministic*, etc. |

    !!! example "Exempel på användning"
        För en **FAQ-assistent**: Använd låg temperature (0.2) och *Factual* behavior.  
        För en **idégenerator**: Använd högre temperature (0.7) och *Creative* behavior.

=== "6. Insights"
    **Insights** ger dig statistik och användardata om hur din assistent används, vilket hjälper dig förbättra den över tid.

    !!! tip "När du bör aktivera Insights"
        Aktivera denna funktion när du vill:
        * Se vilka frågor som återkommer ofta
        * Identifiera områden där assistenten behöver förbättras
        * Mäta hur väl assistenten uppfyller användarbehov
        * Förstå användarnas interaktionsmönster

---

## Hantera assistenter

=== "Byta namn"
    <div class="grid" markdown>
    <div markdown>
    1. Gå till listan **Assistenter**
    2. Klicka på :material-dots-horizontal: bredvid assistenten
    3. Välj **Redigera**
    4. Ändra namn och beskrivning
    5. Klicka på **Spara**
    </div>
    <div markdown>
    ![Redigera assistent](../assets/images/create-assistant-modal.png){ width="300" .shadow }
    </div>
    </div>

=== "Duplicera"
    1. Gå till listan **Assistenter**
    2. Klicka på :material-dots-horizontal: bredvid assistenten
    3. Välj **Duplicera**
    4. Redigera kopian efter behov

    !!! tip "Användbart när"
        Duplicering är perfekt när du vill skapa varianter av samma assistent för olika användningsområden eller testa olika inställningar.

=== "Dela med Space"
    För att göra en assistent tillgänglig för alla medlemmar i ett Space:

    1. Skapa (eller klona) assistenten **inne i** Spacet
    2. Alla medlemmar med rätt behörighet kommer nu att se assistenten
    3. Uppdateringar du gör blir synliga för alla användare

    !!! note "Om Spaces och delning"
        Assistenter skapade i din personliga yta är endast tillgängliga för dig. För att dela med kollegor, använd Spaces. [Läs mer om skillnaden »](skillnad-personlig-vs-space.md)

---

## Vanliga frågor (FAQ)

<div class="grid" markdown>

!!! question "Kan jag återställa en tidigare version av min assistent?"
    Ja, i assistentredigeraren finns fliken *Versions* där du kan se och återställa tidigare versioner av din assistent.

!!! question "Hur tar jag bort en assistent?"
    Gå till assistentlistan, klicka på :material-dots-horizontal: bredvid assistenten och välj **Delete** → bekräfta med **Delete** i dialogrutan.

!!! question "Stöder Intric röstinteraktion med assistenter?"
    Ja, du kan aktivera röstinteraktion genom att bocka i *Enable audio* under *Chat settings* i assistentredigeraren.

!!! question "Kan jag begränsa vilka kunskapskällor min assistent använder?"
    Ja, assistenten använder endast de källor du uttryckligen lägger till i fliken Knowledge.

</div>

---

## Relaterade ämnen
- [Vad är en assistent?](vad-ar-en-assistent.md)
- [Prompt-tekniker för bättre resultat](../prompting/prompt-tekniker.md)
- [Vad är RAG och hur används det?](../kunskapsbaser/vad-ar-rag.md)
- [Skillnad mellan personlig yta och Space](skillnad-personlig-vs-space.md)