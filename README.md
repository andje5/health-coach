# Health Coach Stable v21

Denna version är QA-fokuserad och bygger på Expert v20.

Förbättringar:
- Fixad svensk lokal datumhantering. Health Auto Export-dagar flyttas inte längre en dag bakåt av UTC-konvertering.
- IndexedDB självtest vid start.
- Backup/export och återställning av appdata. Matbilder utelämnas ur backupen för att hålla den liten.
- Lagringskontroll och fallback: måltid kan sparas utan foto om bildlagring slår i kvot.
- Säkrare visning av användartext i måltider.
- Robustare cacheuppdatering/service worker.
- Samma Health Auto Export-import och sammanslagning av överlappande datum.

Rekommenderad synk:
- 1 gång per dag på kvällen för aktuella dagsråd.
- 2–3 gånger per vecka räcker för trenduppföljning.
- Radera ZIP och uppackad JSON från Filer efter att importen är bekräftad.

Kamera:
- Ta foto/Välj bild fungerar och bilden lagras lokalt.
- Automatisk kaloriberäkning från bild ingår inte eftersom gratis-PWA:n saknar en lokal bild-AI-modell/server. Näringsvärden fylls i manuellt.
