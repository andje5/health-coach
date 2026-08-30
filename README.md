# Health Coach v5

Detta är den första samlade versionen som är genomgången mot din riktiga Health Auto Export.

## Det som ingår
- Stabil JSON-import utan externa JavaScript-bibliotek
- IndexedDB för permanent lokal lagring på iPhone
- Nya importer slås ihop med tidigare historik per datum
- Översikt med steg, distans, aktiva kcal, sömn, vilopuls, HRV och VO2 max
- 7-dagars stegdiagram
- Trender för 7/30/90 dagar
- 30-dagars sammanställning
- Viktlogg med historik
- Målvikt och justerbara mål
- Enkel prognos mot målvikt när minst två vägningar finns
- Coach-insikter baserade på gång, sömn, puls, HRV och vikttrend
- Datastatus/diagnostik
- Ingen extern AI eller server; hälsodata stannar lokalt på enheten

## Verifierat mot din export
Filen HealthAutoExport_20260830153351.zip innehåller 31 dagars steg, aktiv energi, aktivitetstid, distans, vilopuls och HRV; 28 sömndagar; 1 VO2 max-värde och 26 träningspass. v5-parsern är byggd för just denna struktur.

## Uppdatera GitHub
1. Packa upp HealthCoachPWA_v5.zip på PC.
2. Ersätt index.html, manifest.json, service-worker.js, icon-192.png och icon-512.png i ditt repository.
3. Commit changes.
4. Vänta 1–3 minuter.
5. Öppna https://andje5.github.io/health-coach/ i Safari på iPhone.
6. Uppdatera tills rubriken visar v5.
7. Stäng hemskärmsappen helt och öppna den igen.
8. Gå till Coach > Välj Health JSON och importera den uppackade JSON-filen.
9. Stäng appen helt och öppna den igen. Datan ska ligga kvar via IndexedDB.

## Fortsatta importer
Importera bara en ny Health Auto Export JSON när du vill uppdatera. v5 slår ihop nya datum med den redan sparade historiken.

## Begränsningar
- Health Auto Export-exporten är fortfarande manuell i gratisupplägget.
- Prognosen för målvikt är en enkel linjär trend och ska ses som riktning, inte ett löfte.
- Coach-insikter är regelbaserade och är inte medicinsk rådgivning.
