# Food AI backend (Level 3)

Frontend v30 is prepared for a POST endpoint that accepts:

```json
{"image":"data:image/jpeg;base64,...","locale":"sv-SE"}
```

and returns:

```json
{
  "name":"Kyckling, ris och broccoli",
  "portion_g":520,
  "kcal":690,
  "protein_g":48,
  "carbs_g":74,
  "fat_g":19,
  "fiber_g":7,
  "confidence_pct":72
}
```

A real Level 3 analysis requires a vision-capable AI service. Keep API keys on the server, never in the PWA.
