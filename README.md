# 🪪 Chuks Obiri — Digital Business Card
### Powered by Sales360-AI

---

## 📁 Files in this package

```
bizcard-vercel/
├── index.html        ← The entire card app (self-contained)
├── manifest.json     ← PWA "Add to Home Screen" config
├── vercel.json       ← Routes, headers, caching, security rules
└── README.md         ← This file
```

> **Optional — for full PWA icon support:**
> - `icon-192.png` (192×192px) — your photo or logo
> - `icon-512.png` (512×512px) — same, larger
>
> Generate both free at: https://realfavicongenerator.net

---

## 🚀 Deploy to Vercel — 3 methods

### Method 1 — Vercel CLI (fastest, ~2 min)

```bash
npm install -g vercel      # one-time install
cd bizcard-vercel
vercel                     # follow the prompts
# → live URL in ~30 seconds
```

To redeploy after edits: `vercel --prod`

---

### Method 2 — GitHub auto-deploy (recommended)

1. Create a new GitHub repo e.g. `chuks-digital-card`
2. Push these files to the repo root:
   ```bash
   git init && git add . && git commit -m "init"
   git remote add origin https://github.com/Tshewin/chuks-digital-card.git
   git push -u origin main
   ```
3. Go to https://vercel.com/new → Import Git Repository → select repo
4. Framework preset: **Other** | Build command: *(blank)* | Output dir: `./`
5. Deploy → every `git push` auto-redeploys ✓

---

### Method 3 — Dashboard drag & drop

1. Go to https://vercel.com/new
2. Scroll to **"Or deploy without Git"**
3. Drag the `bizcard-vercel/` folder into the upload zone
4. Done ✓

---

## 🌐 Custom Domain: `card.sales360-ai.com`

1. Vercel dashboard → Settings → Domains → Add `card.sales360-ai.com`
2. In your DNS provider add:
   ```
   Type: CNAME  |  Name: card  |  Value: cname.vercel-dns.com
   ```
3. SSL auto-provisioned in 2–5 minutes ✓

---

## 📡 NFC Tag Programming

1. Buy NTAG213/NTAG215 NFC stickers (~£1, Amazon)
2. Install **NFC Tools** on Android (free)
3. Write → URL → `https://card.sales360-ai.com`
4. Tap phone to sticker to write → done

---

## ✎ Updating your card

**In-browser (device-only):** tap "✎ Edit Profile" on the card.

**Permanent (all devices):** edit the `defaultProfiles` array in `index.html`, then `git push` — Vercel redeploys in ~10 seconds.

---

## 🔗 After deploying — set your Card URL

1. Open your live card
2. Tap "✎ Edit Profile" → set **Card URL** to `https://card.sales360-ai.com`
3. Save — QR and NFC both now point to your live page ✓

---

Built by Sales360-AI · https://sales360-ai.com
