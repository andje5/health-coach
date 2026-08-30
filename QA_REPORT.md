# Health Coach Stable v21 - QA report

Kontroller genomforda fore leverans:

- `index.html` JavaScript: `node --check` godkand.
- `service-worker.js`: `node --check` godkand.
- Inga dubbla HTML-id:n.
- Alla `$(`-referenser i JavaScript pekar pa befintliga element i HTML.
- Parsern verifierad mot den faktiska Health Auto Export-filen `HealthAutoExport_20260830153351.zip`.
- Verifierade sista varden i exporten:
  - steg: 8405.7167 (2026-08-30)
  - distans: 6.6698 km (2026-08-30)
  - aktiv energi: 2996.1303 kJ = cirka 716 kcal (2026-08-30)
  - aktivitet: 75 min (2026-08-30)
  - somn: 7.0874 h (2026-08-30)
  - vilopuls: 65 bpm (2026-08-30)
  - HRV: 17.961 ms (2026-08-30)
  - VO2 max: 26.67 ml/(kg*min) (2026-08-08)
- Datumhantering korrigerad for svensk lokal tid. Tidigare UTC-konvertering kunde flytta ett midnattsprov en dag bakat.
- Health-import behaller endast relevanta serier och sammanfogar overlappande datum.
- IndexedDB-sjalvtest finns i appen och testar faktisk skrivning/lasning/radering pa enheten.
- Backup/restore finns for health, vikt, installningar och maltidsvarden. Matbilder utelamnas ur backup for att undvika onodigt stora filer.
- Matbilder komprimeras lokalt. Om lagringen ar full forsoker appen spara maltiden utan foto i stallet.
- Anvandarens maltidsnamn HTML-escapas innan visning.
- Service worker ar uppdaterad med network-first for navigation for att minska risken att en gammal appversion fastnar i cache.

Begransning i denna QA-miljo:

Miljon blockerar Chromium/Playwright fran att navigera till bade localhost och file://, sa ett fullstandigt automatiserat Safari/iPhone-liknande end-to-end-test kunde inte koras har. Darfor finns ett inbyggt sjalvtest i appen som kor den kritiska IndexedDB-kontrollen pa den riktiga iPhone-enheten.
