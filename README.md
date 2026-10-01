# 🚂 Vishwajeet Parmar Rajput Train Ticket — Customer Portal

**Owner:** Vishwajeet Parmar Rajput • +91 9530646737 • vishwajeetpar666@gmail.com

A real website (Node.js + Express) for fast Tatkal preparation:

- ✅ Customer registration with **OTP on mobile (SMS) + email**
- ✅ Login (username / email / mobile)
- ✅ Passenger Master List — fill once, copy-paste into IRCTC in one click
- ✅ Train search with **13,500+ Indian railway station codes**
- ✅ Tatkal Quick Kit — passengers copy + direct IRCTC link
- ✅ Owner/Agent panel — all customers, OTP-verified status
- ✅ English + हिंदी

> **Note:** Actual ticket booking and payment happen only on the official
> IRCTC website/app (www.irctc.co.in / RailConnect). This portal prepares
> customers for the fastest legal Tatkal booking.

---

## 🇮🇳 हिंदी में

**यह एक असली वेबसाइट है** (HTML फाइल नहीं) — OTP वेरिफिकेशन, लॉगिन,
पैसेंजर मास्टर लिस्ट और ट्रेन सर्च के साथ। चलाने और इंटरनेट पर लगाने का
पूरा तरीका **README-HINDI.md** में step-by-step लिखा है।

---

## Quick start (local)

```bash
npm install
npm start
# open http://localhost:3000
```

Or on Windows: **double-click `START-WEBSITE.bat`** (installs Node.js prompt if needed).

Until MSG91 / SMTP keys are configured, the OTP is shown on screen (DEV MODE)
so the full flow can be tested.

## Deploy free on Render.com

Option A — **Blueprint (easiest):** render.com → New → **Blueprint** → select this
repo → it reads `render.yaml` → enter your `AGENT_PASSWORD` → Deploy.

Option B — manual: render.com → New → **Web Service** → select repo →
Build: `npm install` • Start: `npm start` → add env vars from `.env.example`.

## Environment variables

| Variable | Meaning |
|---|---|
| `SESSION_SECRET` | Random long text (Render can generate) |
| `AGENT_USERNAME` / `AGENT_EMAIL` / `AGENT_MOBILE` | Owner/agent login details |
| `AGENT_PASSWORD` | Owner password — **change before going live** |
| `MSG91_AUTH_KEY` + `MSG91_TEMPLATE_ID` | Real OTP on mobile (msg91.com, paid) |
| `SMTP_HOST` / `SMTP_PORT` / `SMTP_USER` / `SMTP_PASS` / `MAIL_FROM` | Real OTP on email (Gmail App Password) |

See `.env.example` for the full template.

## Project structure

```
├── server.js          → backend: API, OTP, database, security
├── public/
│   ├── index.html     → frontend (English + हिंदी)
│   └── stations.json  → 13,500+ stations
├── render.yaml        → one-click deploy config for Render.com
├── START-WEBSITE.bat → Windows double-click starter
└── data/              → JSON database (auto-created)
```
