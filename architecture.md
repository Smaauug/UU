# Arkitektur: UU Ekonomikandidat-Assistent

Detta projekt är optimerat för att fungera som en intelligent studieassistent i terminalen. Strukturen är byggd för att maximera agentens förmåga att snabbt hitta relevant kursmaterial utan onödig token-konsumtion.

## Projektstruktur

```text
/
├── agents.md          # Definitioner av agentens personligheter och expertområden.
├── setup.md           # Installationsguide för Hanna (Queen of the Terminal).
├── architecture.md    # Denna fil - teknisk överblick.
├── GEMINI.md          # Systeminstruktioner och operativa mandat.
├── text.md            # Policy för hur text och filer sparas.
├── context/           # Central lagringsplats för litteratur och anteckningar.
│   ├── index.md       # "Hjärnan" i biblioteket. Mappar innehåll för snabb sökning.
│   └── [KURSKOD]/     # Undermappar som skapas automatiskt (t.ex. FEK_A, NEK_B).
└── output/            # Plats för alla genererade filer (uppsatser, utkast, etc.)

```

## Sökstrategi (Index-driven)

För att undvika att agenten läser igenom stora PDF-filer i onödan, använder vi en **Index-First**-metod:

1. **Index-filen**: `/context/index.md` innehåller metadata om alla filer i `/context/`. Den listar ämnen, kapitel och centrala koncept som täcks i varje dokument.
2. **Arbetsflöde**: Agenten MÅSTE alltid börja med att läsa `/context/index.md` när en fråga om kursinnehåll ställs.
3. **Målmedveten läsning**: Baserat på indexet kan agenten sedan navigera direkt till rätt fil för att ge precisa svar.

## Skrivstrategi

Alla filer som agenten skapar eller redigerar ska hamna i `/output/`. Agenten ska följa policyn i `text.md` för att säkerställa att inget material går förlorat och att versioner hanteras korrekt.
