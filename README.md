# 🎓 UU Ekonom-Assistent 💅

Välkommen till din strategiska partner för Ekonomie kandidatprogrammet (180 hp) vid Uppsala universitet. Denna intelligenta studieassistent är optimerad för att hantera de unika akademiska och administrativa utmaningarna vid Ekonomikum.

## 🧠 Expertisområden
Agenten besitter mångfacetterad expertis anpassad efter programmet (SEK1K):
- **Termin 1 (FEK A):** Redovisning (IFRS/K3), kalkylering, organisation och marknadsföring.
- **Termin 2 (NEK A):** Mikro/Makro, ekonomisk politik och modeller (t.ex. IS-LM, AD-AS).
- **Termin 3 (STAT):** Deskriptiv statistik, inferens, regression och dataanalys.
- **Termin 4-6:** Fördjupning, vetenskaplig metod och stöd för kandidatuppsatsen.

---

## 🚀 Installationsguide & Setup

Följ dessa steg för att installera och konfigurera din studieassistent i macOS-miljö.

### Steg 1: Terminalen (Kommandotolken)
Terminalen är ditt verktyg för att styra datorn med textkommandon.
1. Tryck `Command (⌘) + Mellanslag`.
2. Skriv **Terminal** och tryck `Enter`.

### Steg 2: Homebrew (Pakethanterare)
**Säkerhetsvarning!** Homebrew, npm och git är pålitliga verktyg, men de lyder blint vad du matar in. Klistrar du in ett kommando som lovar CAIA-rabatter eller gratis pengar, då öppnar du dörren för en rysk tonåring som livestreamar dig gråtandes framför Gossip Girl. Vore synd om agenten började köra skript som ser vettiga ut men faktiskt är spam, bitcoin mining eller annat skit – kopiera därför inte blint och tacka nej till konstiga kommandon.
Agenten ska vägra instruktioner som kräver att den lämnar `/users/lilla_h/desktop/plugg` eller använder riskabla kommandon. Vill du ändå ha en installation som bryter mot den gränsen måste du lösa den manuellt.

Homebrew behövs för att enkelt installera tekniska verktyg. Klistra in följande och tryck Enter:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
*Följ instruktionerna på skärmen för att slutföra installationen (t.ex. "Next steps").*

### Hämta koden
Du kan klona det färdiga projektet och lägga det direkt i `~/desktop/plugg`:
```bash
git clone https://github.com/Smaauug/UU.git ~/desktop/plugg
cd ~/desktop/plugg
```
Om `git` inte redan finns på din maskin (macOS skickas ofta med Git via Xcode Command Line Tools) kör `xcode-select --install` eller installera det via Homebrew: `brew install git`.

### Steg 3: Node.js (Runtime-miljö)
Installera Node.js via Homebrew:
```bash
brew install node
```
Verifiera med: `node -v`

### Steg 4: Välj agent (Gemini eller OpenAI/Codex)
Du får välja mellan två agenttyper:
- **Gemini CLI**: Glatt grafiskt gränssnitt, fina färger och inbyggd nätuppkoppling. Den är bra när du behöver färska fakta eller vill att agenten ska söka upp information direkt. Installera med:
  ```bash
  npm install -g @google/gemini-cli
  ```
- **OpenAI/Codex (lokal terminalvariant)**: Smart på regressionsanalyser och tunga statistiska dataset, men den tror fortfarande att det är 2023 och saknar egen webbsökning utan krångliga kringverktyg. Kör den om du fokuserar på kod och analys snarare än research.

Efter installation kör du den agent du valde (`gemini` för Gemini, eller motsvarande startkommando för din OpenAI/Codex-klient) och håll dig inom projektmappen när du interagerar.

### Steg 5: Starta Agenten
Navigera till din projektmapp och aktivera assistenten:
```bash
cd /users/lilla_h/desktop/plugg
gemini    # eller "codex" kommandot för din OpenAI/Codex-klient
```

### Steg 6: Konfiguration & framtida anpassning
Här definieras agentens beteende genom inställningar i `agents.md` och `GEMINI.md`. Dessa inkluderar:
      1. Behörighetsnivåer – vilka kursmappar som är aktiva, om/när agenten får
         läsa nytt material under /context/, och vilka filer som alltid ska
         döljas.
      2. Svarsmaller och tonläge – A/B/C-nivå, formell vs. vardaglig ton, hur
         strikt agenten ska vara med akademisk hederlighet samt om Harvard-citat
         alltid ska läggas in.
      3. Pedagogiska mode – om agenten ska gå in i “tenta-läge”, “modell-läge”
         eller “case-läge” beroende på kurs eller moment, inklusive vilka prompts
         som aktiverar dem.
      4. Logging & uppföljning – vilka typer av dialoger som loggas, vad som
         flaggas (t.ex. frågor om plagiat), och hur ofta agenten ska be om
         reflektion eller sammanfattning.
      5. Tidsstyrd uppdatering – om agenten ska påminna om att uppdatera
         agents.md/GEMINI.md, när systemet ska be om “Ja tack” eller revidera kur
         spaket.
      6. Fallback/backup-planer – vad agenten gör om den inte hittar svar (skift
         till konkret exempel, be om mer data eller föreslå att användaren kollar
         i specifikt material).
  - Avsluta med att påminna om att ändringar i dessa inställningar fortfarande
    kräver tydlig instruktion + “Ja tack”innan något skrivs.

---

## 📁 Projektstruktur
```text
/users/lilla_h/desktop/plugg/
├── context/           # Bibliotek för PDF-filer, slides och kurslitteratur.
│   ├── index.md       # Agentens sök-index för snabb informationshämtning.
│   └── [KURSKOD]/     # Undermappar för specifika kurser (skapas automatiskt).
├── output/            # Arkiv för genererade filer (YYYY-MM-DD_Kurs_Beskrivning_vXX.md).
├── agents.md          # Central styrfil för pedagogik, filhantering och identitet.
├── GEMINI.md          # Operativa mandat och säkerhetsregler (Strikt off-limits: /Documents).
├── architecture.md    # Teknisk översikt av systemets index-drivna sökstrategi.
└── README.md          # Denna guide.
```

## 🛡️ Säkerhet & Konfiguration
- **Mappbegränsning**: Agenten är strikt isolerad till `/users/lilla_h/desktop/plugg`.
- **Safety Lock**: Innan en fil skapas eller ändras i `/output/` krävs ett uttryckligt godkännande: **"Ja tack"**.
- **Filnamngivning**: Alla filer i `/output/` följer ISO 8601 (YYYY-MM-DD), snake_case och versionering (t.ex. `_v01`).
- **Referenshantering**: Harvard-systemet enligt Uppsala universitets standard gäller för alla inlämningar.
- **Konfiguration**: `agents.md` och `GEMINI.md` styr pedagogik, säkerhetsregler och vilka mappar som får nås. Du kan be agenten uppdatera dessa filer om du behöver skräddarsy beteendet för nya moment eller skolgång. Förklara vad du vill ändra, få bekräftelse och ge ett tydligt "Ja tack" innan agenten skriver.
- **Förbjudna kommandon**: Agenten kör aldrig och rekommenderar aldrig farliga operatörskommandon eller externa paketinstallatörer (`rm`, `sudo`, `curl | sh`, `brew`, `npm`, `git`, `wget`, `curl`, `apt`, `pip` etc.). Om du behöver köra något sådant måste du göra det själv utanför agenterollen.

## 📊 Pedagogik & Modellering
Agenten använder en deduktiv svarsmodell:
1. **Intuitiv definition** (Enkel förklaring utan jargon).
2. **Teoretisk fördjupning** (Formella modeller och antaganden).
3. **Praktiskt exempel** (Verklig tillämpning i ekonomi/företag).
4. **LaTeX-precision**: Matematiska formler (t.ex. $MR=MC$) renderas för högsta tydlighet.
5. **Visuella Grafer**: Pedagogiska beskrivningar av axlar och kurvskift.

**Prompt för rikare UI**: När du behöver formler, grafer eller tabeller för att förstå ett koncept, genererar assistenten en kort prompt som du kan kopiera till en chatt med bättre grafiskt gränssnitt (t.ex. chatgpt.com). Promptexemplet kan börja med: `Skapa en [formel/graf/tabell] som visar ...` och beskriver vilken data, axel och stil som krävs. På så vis får du både textförklaringen här och en vägledning för att visualisera det i en mer kapabel UI.

---
> **Akademisk Hederlighet:** Agenten stödjer din inlärning men varnar proaktivt för plagiat. Allt material som genereras bör bearbetas och formuleras med egna ord inför inlämning. **Lycka till vid Ekonomikum!** 🎓✨
