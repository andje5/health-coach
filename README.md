# Health Coach v3.2

Fix för felet "The quota has been exceeded".

Orsak:
v3.1 försökte spara hela Health Auto Export JSON-filen i webbläsarens localStorage.
Din export är mycket större än localStorage-kvoten på iPhone.

Lösning:
v3.2 läser fortfarande hela JSON-filen, men behåller bara de relevanta 30-dagarsserierna:
- steg
- gång/löpdistans
- aktiv energi
- träningsminuter
- sömn
- vilopuls
- HRV
- VO2 max
- vikt om body_mass finns

GPX och övriga rådata sparas inte i webbläsaren.

## Uppdatera GitHub
1. Packa upp HealthCoachPWA_v3_2.zip.
2. Ersätt filerna i github.com/andje5/health-coach.
3. Commit changes.
4. Vänta 1–3 minuter.
5. Stäng Health Coach helt på iPhone och öppna igen.
6. Om den gamla versionen ligger kvar: öppna sidan i Safari, uppdatera, och starta sedan hemskärmsappen igen.

## Innan ny import
Tryck "Rensa hälsodata" en gång så eventuella gamla poster tas bort.

## Import
1. Packa upp Health Auto Export ZIP i Filer.
2. Öppna Health Coach.
3. Tryck "Välj Health JSON".
4. Välj den stora JSON-filen.
5. Vänta på meddelandet "Klart".

All tolkning sker lokalt på iPhone.
