# Health Coach v3.3

Detta är den riktiga fixen för "The quota has been exceeded".

Felet i v3.2:
v3.2-paketet innehöll av misstag fortfarande den gamla importkoden och försökte spara hela Health Auto Export-filen. Därför fick du samma kvotfel.

v3.3:
- läser hela JSON-filen från Filer
- behåller endast 9 relevanta mätserier
- sparar bara cirka några tiotal kB i localStorage
- sparar inte GPX, råa träningspass eller övriga HealthKit-serier
- visar storleken på den sparade kompakta datan efter lyckad import

## Uppdatera
1. Packa upp HealthCoachPWA_v3_3.zip på PC.
2. Ersätt filerna i GitHub-repot.
3. Commit changes.
4. Vänta 1–3 minuter.
5. På iPhone: öppna sidan i Safari och uppdatera den.
6. Stäng hemskärmsappen helt och öppna den igen.
7. Tryck "Rensa hälsodata".
8. Tryck "Välj Health JSON".
9. Välj HealthAutoExport-2026-07-31-2026-08-30.json.

Efter lyckad import ska statusraden visa antal relevanta hälsomått, träningspass och hur många kB som sparades.
