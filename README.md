# Health Coach v4

Nyckelförbättring:
Health-data sparas nu i IndexedDB istället för localStorage.

Det betyder:
- importera JSON en gång
- stäng appen
- öppna den igen
- datan ska ligga kvar

IndexedDB klarar betydligt större datamängder än localStorage och är rätt väg för en PWA på iPhone.

## Uppdatera
1. Packa upp HealthCoachPWA_v4.zip på PC.
2. Ersätt filerna i GitHub-repot.
3. Commit changes.
4. Vänta 1–3 minuter.
5. Öppna GitHub Pages-adressen i Safari och uppdatera.
6. Stäng hemskärmsappen helt och öppna den igen.
7. Importera Health JSON en gång.
8. Stäng Health Coach helt.
9. Öppna den igen och kontrollera att datan fortfarande finns kvar.

## Viktigt
Vikt sparas fortfarande separat i localStorage eftersom den bara är ett par små värden och inte orsakar kvotproblem.

Nästa utvecklingssteg:
- viktgraf
- 7/30/90-dagarstrender
- prognos mot 95 kg
- bättre coach-insikter
- enklare ny-import där nya dagar läggs till i historiken
