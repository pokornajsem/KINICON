# KINICON (v1.0)

Moderní webová aplikace pro image-to-video generování s pedagogickým modulem.

## Funkce

- Drag-and-drop uploader pro obrázky
- Připravené `API` rozhraní pro Image-to-Video (Hugging Face / Google Labs / jiná služba)
- „Stateless“ zpracování: obrázky se neukládají natrvalo (jen v paměti)
- Edukační karty uměleckých směrů pro žáky 3. třídy
- `Info pro učitele` (Bring Your Own Tokens + bezpečnostní prvky)

## Lokální spuštění

1. V terminálu v projektu:
   - `npm install`
   - `npm run dev`
2. Otevři `http://localhost:3000`

## Proměnné prostředí (volitelné, ale nutné pro skutečné generování)

Vytvoř soubor `.env.local`:

```bash
IMAGE_TO_VIDEO_ENDPOINT="https://your-image-to-video-endpoint.example.com"
IMAGE_TO_VIDEO_API_KEY="YOUR_API_KEY_IF_NEEDED"
IMAGE_TO_VIDEO_MODEL="optional-model-name"
```

Pozn.: Payload se může lišit podle zvolené Image-to-Video služby. Serverová cesta je připravená – uprav v `src/app/api/image-to-video/route.ts` dle dokumentace upstream API.

## Nasazení na Vercel

1. Propojit GitHub v Cursor / Vercel
2. Na Vercel zvolit `Add New -> Project -> Import -> Deploy`
3. V `Settings -> Environment Variables` nastavit proměnné z části výše

