# guns.lol — Personal Bio Link Page

A fully functional, single-file bio link page inspired by the guns.lol aesthetic. Dark theme, neon purple accents, glitch effects, music player, visitor logger, and a hidden admin panel.

## 🚀 Features

- **Dark neon design** — Purple theme with 3 alternative colors (blue, green, pink)
- **Glitch title** — Animated glitch effect on the header
- **Socials** — Steam, GitHub, Spotify links with hover tooltips
- **Currently Playing** — Display your current game
- **Commissions** — Status badge (Open/Closed)
- **Music Player** — Lo-fi playlist with 5 tracks, wave visualizer, play/pause
- **PC Specs** — Collapsible accordion with your hardware info
- **Contact** — Copy-to-clipboard buttons for Discord and Email
- **Share** — Web Share API with clipboard fallback
- **Live Clock** — Real-time digital clock and date in the footer
- **Visit Counter** — Powered by countapi.xyz (free)
- **Matrix Rain** — Subtle background effect (toggleable)
- **Floating Particles** — Ambient particle animation
- **CRT Scanlines** — Subtle overlay effect
- **Fully Responsive** — From 320px mobile to 4K desktop

## 🔐 Hidden Admin Panel

A password-protected admin dashboard that logs every visitor's data.

### How to access:
1. **Click the title "guns.lol" 7 times** (rapidly)
2. Enter the password: **`knssfplf`**
3. The admin panel opens with all visitor logs

### What data is captured:
| Data | Source |
|------|--------|
| IP Address | api.ipify.org |
| City / Region / Country | ip-api.com (free) |
| ISP / Organization | ip-api.com |
| Date & Time | Local timestamp (BR timezone) |
| Screen Resolution | `screen.width x screen.height` |
| Browser Language | `navigator.language` |
| Referrer URL | `document.referrer` |
| User-Agent | `navigator.userAgent` |
| Page URL | `window.location.href` |

### Admin panel features:
- **Statistics cards** — Total visits, today's visits, unique IPs
- **Log list** — Last 50 visitors displayed with all details
- **Discord Webhook** — Paste a Discord webhook URL to receive real-time visit alerts
- **Export JSON** — Download all logs as a JSON file
- **Clear Logs** — Delete all stored logs

## 🎵 Music

The player cycles through 5 lo-fi instrumental tracks (~3 min each) from SoundHelix (free music). The playlist auto-advances when a track ends.

To use your own music, edit the `MUSIC_PLAYLIST` array in the JavaScript section. You can host MP3s for free on:
- [Catbox.moe](https://catbox.moe) — up to 200MB per file
- Discord CDN — upload to any channel and copy the link
- [SoundHelix](https://www.soundhelix.com) — free sample tracks

## 🛠️ Customization

All editable fields are marked with `<!-- 👇 EDITAR AQUI -->` in the HTML. The main JavaScript variables at the top:

```javascript
const USERNAME = "knssfplf";
const STEAM_ID = "76561199658376471";
const GITHUB = "knssfplf";
const CURRENT_GAME = "Counter-Strike 2";
const ADMIN_PASSWORD = "knssfplf";     // change this!
const MUSIC_PLAYLIST = [ /* ... */ ];
const PC_SPECS = { /* ... */ };
```

You'll also need to replace:
- Avatar image URL (search for `pravatar.cc`)
- Discord/Email contact info (search for `data-copy`)
- Social media links
- Wallpaper link
- Open Graph image URL

## 📡 Discord Webhook Setup

1. Open Discord → Server Settings → Integrations → Webhooks
2. Create a new webhook and copy the URL
3. Open your site → click the title 7 times → enter password
4. Paste the webhook URL in the admin panel and click "Save"
5. Every new visitor will send an embed to your Discord channel

## 🌐 Deployment (Free)

### Option 1: GitHub Pages (recommended)
1. Create a repository named `guns` (or any name)
2. Upload `index.html` and `README.md` to the repository
3. Go to Settings → Pages → Select branch `main` / folder `/`
4. Your site is live at: `https://yourusername.github.io/guns/`

### Option 2: Netlify
1. Go to [app.netlify.com](https://app.netlify.com)
2. Drag & drop the folder containing `index.html`
3. Netlify generates a URL instantly

### Option 3: Vercel
1. Install Vercel CLI: `npm i -g vercel`
2. Run `vercel` in the project folder
3. Follow the prompts

## 📁 File Structure
```
guns.lol/
├── index.html    # Complete site (HTML + CSS + JS all in one file)
└── README.md     # This documentation
```

No external files needed — everything is embedded in `index.html`.

## 🔒 Privacy Notes
- Visitor data is stored in your browser's **localStorage** (only you can see it via the admin panel)
- IP and location are fetched via free public APIs (ipify.org, ip-api.com)
- No data is sent to third parties unless you configure a Discord webhook
- The visit counter uses countapi.xyz (anonymous, just a number)

---

**Made with 💜 by knssfplf**
