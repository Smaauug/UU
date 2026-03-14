# UU Ekonom‑Assistent

Denna assistent är utformad som ett stödverktyg för studenter vid Ekonomie kandidatprogrammet (180 hp) vid Uppsala universitet. Syftet är att underlätta studier, strukturera kursmaterial och ge pedagogiska förklaringar inom centrala delar av utbildningen.

## Expertisområden
Agenten är anpassad efter programmets huvudsakliga kursstruktur (SEK1K):

- **Termin 1 (FEK A):** Redovisning (IFRS/K3), kalkylering, organisation och marknadsföring.
- **Termin 2 (NEK A):** Mikroekonomi, makroekonomi, ekonomisk politik och modeller (t.ex. IS‑LM och AD‑AS).
- **Termin 3 (STAT):** Deskriptiv statistik, statistisk inferens, regression och dataanalys.
- **Termin 4–6:** Fördjupningskurser, vetenskaplig metod samt stöd vid arbete med kandidatuppsats.

---

## Installationsguide

Följ nedanstående steg för att installera och konfigurera assistenten i en macOS‑miljö.

### Steg 1: Öppna Terminal
Terminalen används för att köra textbaserade kommandon i operativsystemet.

1. Tryck `Command (⌘) + Mellanslag`.
2. Skriv **Terminal** och tryck `Enter`.

### Steg 2: Installera Homebrew
Homebrew är en pakethanterare som används för att installera utvecklingsverktyg i macOS.

Kör följande kommando i terminalen:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Följ därefter instruktionerna som visas i terminalen.

### Hämta projektet
Kloning av projektet görs med Git. Följande kommando laddar ner projektet till katalogen `~/desktop/plugg`.

```bash
git clone https://github.com/Smaauug/UU.git ~/desktop/plugg
cd ~/desktop/plugg
```

Om `git` saknas kan det installeras via:

```bash
xcode-select --install
```

eller via Homebrew:

```bash
brew install git
```

### Steg 3: Installera Node.js
Node.js används som körmiljö för agenten.

Installera via Homebrew:

```bash
brew install node
```

Verifiera installationen:

```bash
node -v
```

### Steg 4: Välj agent
Projektet kan användas tillsammans med olika CLI‑baserade AI‑agenter.

**Gemini CLI**

Installera med:

```bash
npm install -g @google/gemini-cli
```

Gemini CLI lämpar sig särskilt väl när aktuell information eller nätbaserad sökning behövs.

**OpenAI / Codex (lokal terminalvariant)**

Denna variant är främst lämplig för kodrelaterade uppgifter, dataanalys och statistiska beräkningar.

Efter installation startas vald agent från projektmappen.

### Steg 5: Starta assistenten
Navigera till projektmappen och starta agenten:

```bash
cd /users/lilla_h/desktop/plugg
gemini
```

Om en annan CLI‑agent används startas den med motsvarande kommando.

### Steg 6: Konfiguration
Agentens beteende styrs huvudsakligen genom konfigurationsfilerna `agents.md` och `GEMINI.md`.

Dessa filer definierar bland annat:

1. **Behörigheter** – vilka mappar och filer agenten får läsa.
2. **Svarsmallar och tonläge** – hur förklaringar struktureras och vilken akademisk nivå som eftersträvas.
3. **Pedagogiska lägen** – exempelvis tentaförberedelse, modellanalys eller fallstudier.
4. **Loggning och uppföljning** – hur dialoger och interaktioner dokumenteras.
5. **Systemuppdateringar** – när konfiguration bör revideras eller uppdateras.
6. **Fallback‑strategier** – hur agenten agerar när tillräcklig information saknas.

Ändringar i dessa filer bör göras med tydliga instruktioner och bekräftas innan de skrivs till disk.

---

## Projektstruktur

```
/users/lilla_h/desktop/plugg/
├── context/           # Bibliotek för kursmaterial, exempelvis PDF‑filer och föreläsningsslides
│   ├── index.md       # Index för snabb informationssökning
│   └── [KURSKOD]/     # Undermappar för specifika kurser
├── output/            # Genererade filer (YYYY-MM-DD_kurs_beskrivning_vXX.md)
├── agents.md          # Central konfigurationsfil för pedagogik och identitet
├── GEMINI.md          # Operativa regler och säkerhetsbegränsningar
├── architecture.md    # Teknisk översikt av systemets struktur
└── README.md          # Dokumentation
```

---

## Säkerhet och konfiguration

- **Mappbegränsning:** Agenten är avsedd att arbeta inom katalogen `/users/lilla_h/desktop/plugg`.
- **Bekräftelsekrav:** Innan filer skapas eller ändras i `/output/` krävs en uttrycklig bekräftelse.
- **Filnamnsstandard:** Filer följer ISO‑8601‑datumformat och versionsnumrering.
- **Referenshantering:** Harvard‑systemet enligt Uppsala universitets riktlinjer används vid akademiskt arbete.

---

## Pedagogisk struktur

Agenten använder en strukturerad förklaringsmodell:

1. **Intuitiv definition** – en kort och begriplig introduktion.
2. **Teoretisk fördjupning** – formella modeller och antaganden.
3. **Praktiskt exempel** – tillämpning i ekonomiska eller företagsekonomiska sammanhang.

Matematiska uttryck kan presenteras med LaTeX‑notation för tydlighet.

---

## Akademisk hederlighet

Assistenten är avsedd som ett stöd för lärande. Allt material som genereras bör granskas och omformuleras av studenten innan det används i akademiska inlämningar.
