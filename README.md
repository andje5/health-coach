# Health Coach v30 Food AI

This version keeps the stable Health Auto Export flow and adds the full food-camera UX.

What works without any paid AI service:
- Take food photo with iPhone rear camera
- Compress preview locally
- Save meals, images, kcal and macros locally in IndexedDB
- Daily food totals
- Meal history and deletion
- Manual correction before saving

What requires an AI backend:
- Automatic food identification from the image
- Portion-size estimation
- Automatic kcal/protein/carbs/fat/fiber estimate

Why:
A PWA cannot securely embed an AI provider API key. A real Level 3 function therefore needs a server-side endpoint. v30 is already wired for such an endpoint.

Health-data import remains unchanged:
Health Auto Export -> JSON ZIP -> unpack -> import JSON in Health Coach.
