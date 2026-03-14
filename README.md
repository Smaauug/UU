# 🎓 UU Ekonom-Assistent (Hanna Edition) 💅

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
Homebrew behövs för att enkelt installera tekniska verktyg. Klistra in följande och tryck Enter:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
*Följ instruktionerna på skärmen för att slutföra installationen (t.ex. "Next steps").*

### Steg 3: Node.js (Runtime-miljö)
Installera Node.js via Homebrew:
```bash
brew install node
```
Verifiera med: `node -v`

### Steg 4: Gemini CLI (AI-gränssnittet)
Installera det officiella gränssnittet globalt:
```bash
npm install -g @google/gemini-cli
```

### Steg 5: Starta Agenten
Navigera till din projektmapp och aktivera assistenten:
```bash
cd /users/lilla_h/desktop/plugg
gemini
```

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

## 🛡️ Säkerhet & Digital Ordning
- **Mappbegränsning**: Agenten är strikt isolerad till `/users/lilla_h/desktop/plugg`.
- **Safety Lock**: Innan en fil skapas eller ändras i `/output/` krävs ett uttryckligt godkännande: **"Ja tack"**.
- **Filnamngivning**: Alla filer i `/output/` följer ISO 8601 (YYYY-MM-DD), snake_case och versionering (t.ex. `_v01`).
- **Referenshantering**: Harvard-systemet enligt Uppsala universitets standard är förvalt.

## 📊 Pedagogik & Modellering
Agenten använder en deduktiv svarsmodell:
1. **Intuitiv definition** (Enkel förklaring utan jargon).
2. **Teoretisk fördjupning** (Formella modeller och antaganden).
3. **Praktiskt exempel** (Verklig tillämpning i ekonomi/företag).
4. **LaTeX-precision**: Matematiska formler (t.ex. $MR=MC$) renderas för högsta tydlighet.
5. **Visuella Grafer**: Pedagogiska beskrivningar av axlar och kurvskift.

---
> **Akademisk Hederlighet:** Agenten stödjer din inlärning men varnar proaktivt för plagiat. Allt material som genereras bör bearbetas och formuleras med egna ord inför inlämning. **Lycka till vid Ekonomikum!** 🎓✨
