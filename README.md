
# Health Coach PWA – gratisversion

Detta är en fristående webbapp som kan läggas på iPhone-hemskärmen och öppnas som en app.

## Vad den gör
- Dashboard för steg, aktiva kalorier, träningsminuter, sömn, vilopuls, HRV, VO₂ max och senaste träningspass.
- Enkel readiness score.
- Lokala coach-insikter.
- 7-dagars stapeldiagram.
- Data sparas lokalt i iPhone-webbläsaren.
- Tar emot JSON via URL-parametern `data`.

## Viktig begränsning
En webbapp får inte läsa Apple Health/HealthKit direkt. Därför behöver en iPhone-genväg hämta värden från Hälsa och öppna webbappen med ett JSON-paket.

## Publicera gratis från Windows med GitHub Pages
1. Skapa ett gratis konto på github.com om du inte redan har ett.
2. Skapa ett nytt repository, exempelvis `health-coach`.
3. Ladda upp alla filer från denna mapp i repositoryts rot.
4. Gå till Settings > Pages.
5. Under Build and deployment välj Deploy from a branch.
6. Välj branch `main` och folder `/ (root)`, spara.
7. Efter någon minut får du en HTTPS-adress till appen.
8. Öppna adressen i Safari på iPhone.
9. Tryck Dela > Lägg till på hemskärmen.

## Första testet
Tryck "Visa demo" i appen.

## Koppla en iPhone-genväg
Apple Genvägar kan läsa vissa värden från Hälsa. Exakta åtgärdsnamn kan variera med iOS-version och språk.

Målet är att skapa ett Dictionary med dessa nycklar:
- steps
- activeEnergyKcal
- exerciseMinutes
- sleepHours
- restingHeartRate
- hrvMs
- vo2Max
- latestWorkoutMinutes

Konvertera dictionaryn till JSON-text och URL-koda texten. Öppna sedan:
`DIN_APP_URL/?data=URLKODAD_JSON`

När appen öppnas läser den JSON-paketet och sparar värdena lokalt.

## Säkerhet
Den här versionen skickar inte hälsodata till någon server och innehåller ingen extern AI-anslutning. All analys körs lokalt i webbläsaren.
