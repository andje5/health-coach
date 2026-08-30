# Health Coach v3.4

Detta är kvotfixen som helt tar bort Health-data från localStorage.

Din export har bara cirka 31 dagsposter för de relevanta måtten, så själva datamängden är inte problemet. Felet kommer från Safari/PWA-lagringen på iPhone.

v3.4:
- läser JSON-filen direkt från Filer
- filtrerar till relevanta mått
- renderar dashboarden direkt i minnet
- skriver INTE Health-data till localStorage
- kan därför inte få QuotaExceededError från Health-importen

Nackdel:
Om appen stängs helt behöver JSON-filen importeras igen. När importen fungerar stabilt kan vi senare lägga persistent lagring i IndexedDB.

## Uppdatering
1. Packa upp v3.4.
2. Ersätt filerna i GitHub-repot.
3. Commit.
4. Vänta 1-3 minuter.
5. Öppna GitHub Pages-adressen i Safari och uppdatera.
6. Stäng hemskärmsappen helt och öppna igen.
7. Tryck Rensa hälsodata.
8. Tryck Välj Health JSON.
9. Välj samma uppackade JSON-fil.
