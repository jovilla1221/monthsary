# 🎀 Happy Monthsary — Coquette Web

Web interaktif monthsary coquette pink. Slide-based, PIN lock screen, hujan love, polaroid scrapboard gallery, typewriter letter.

## Flow

```
🔒 LOCK SCREEN (PIN 6 digit) → 🎀 COVER → 📅 COUNTER → 📖 STORY → 📌 GALLERY → 💌 LETTER
```

## Lokasi

| Item | Path |
|------|------|
| Source | `/home/ec2-user/projects/monthsary/index.html` |
| Live | https://monthsary-eight-plum.vercel.app |
| GitHub | (belum) |

## Personalisasi

Buka file, edit bagian `const C = {...}` di `<script>`:

- `startDate` — YYYY-MM-DD (counter + PIN hint)
- `pin` — 6 digit PIN buka web
- `coverTitle`, `coverSub` — teks cover
- `ytId` — YouTube video ID (opsional)
- `story` — array of {tag, title, text}
- `gallery` — array of {cap, note?, img, tape?, wide?}
- `letter` — array of string

## Deploy ulang

```bash
export VERCEL_TOKEN="$(grep VERCEL_TOKEN /home/ec2-user/.hermes/.env | head -1 | cut -d= -f2)"
cd /home/ec2-user/projects/monthsary
vercel --yes --token "$VERCEL_TOKEN" --prod
```