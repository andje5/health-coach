# Health Coach v3.1

Fix för iPhone-import.

Varför ändringen:
v3 försökte läsa ZIP-filen med ett externt JavaScript-bibliotek. På iPhone/PWA kan det biblioteket ibland inte laddas, vilket gav "Import misslyckades".

v3.1 behöver inget externt ZIP-bibliotek. iPhone packar upp ZIP-filen först och Health Coach läser sedan JSON-filen direkt.

## Uppdatera GitHub
1. Packa upp HealthCoachPWA_v3_1.zip på PC.
2. Öppna github.com/andje5/health-coach
3. Ersätt index.html, manifest.json, service-worker.js, icon-192.png och icon-512.png.
4. Commit changes.
5. Vänta 1–3 minuter.
6. Öppna Health Coach på iPhone igen.

## Importera på iPhone
1. Öppna Filer.
2. Leta upp HealthAutoExport_....zip.
3. Tryck en gång på ZIP-filen. iPhone skapar en uppackad mapp bredvid.
4. Öppna mappen.
5. Där finns GPX-filer och en stor fil som heter ungefär:
   HealthAutoExport-2026-07-31-2026-08-30.json
6. Öppna Health Coach.
7. Tryck "Välj Health JSON".
8. Välj den stora JSON-filen.
9. Vänta medan cirka 18 MB JSON läses.
10. När importen är klar fylls dashboarden.

All bearbetning sker lokalt i Safari/PWA.
