# Health Coach v3

Denna version kan importera ZIP-exporten direkt från Health Auto Export i Safari/iPhone.

## Uppdatera GitHub
1. Packa upp denna ZIP på PC.
2. Öppna github.com/andje5/health-coach
3. Ladda upp/ersätt index.html, manifest.json, service-worker.js, icon-192.png och icon-512.png.
4. Commit changes.
5. Vänta 1–3 minuter.
6. Öppna https://andje5.github.io/health-coach/ på iPhone.
7. Om gammal version visas: stäng appen helt och öppna igen, eller öppna sidan i Safari och uppdatera.

## Import på iPhone
1. I Health Auto Export: skapa en manuell ZIP/JSON-export.
2. Spara ZIP-filen i Filer på iPhone.
3. Öppna Health Coach.
4. Tryck "Välj Health ZIP".
5. Välj ZIP-filen.
6. Vänta tills appen säger att importen är klar.

All JSON-tolkning sker lokalt i webbläsaren. Appen skickar inte ZIP-filen till en server.

## Format som stöds
Formatet i filen HealthAutoExport_20260830153351.zip:
- data.metrics
- data.workouts

Mått som används:
- step_count
- walking_running_distance
- active_energy
- apple_exercise_time
- sleep_analysis
- resting_heart_rate
- heart_rate_variability
- vo2_max

Vikt finns inte i den exporterade filen som analyserades, därför registreras den manuellt tills body_mass finns i framtida exporter.
