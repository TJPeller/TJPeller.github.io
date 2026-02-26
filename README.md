# PAS Concierge — Payment System

Branded, secure invoice and payment system for PAS Concierge travel services.

## Pages

| File | Purpose | Who Sees It |
|------|---------|-------------|
| `index.html` | Landing page with navigation | Public |
| `pay.html` | Client payment page (demo + dynamic) | Clients |
| `success.html` | Payment confirmation with receipt | Clients |
| `admin.html` | Invoice creation, link generation, tracking | Admin only |

## Quick Start

1. Clone this repo
2. Drop `PAS_LOGO.png` into `assets/`
3. Push to GitHub → Enable Pages in Settings
4. Done — live at `username.github.io`

## How It Works

- Admin opens `admin.html` → creates invoice → gets unique payment link
- Client opens their link → sees branded page with locked amount → clicks Pay
- System marks invoice as paid → client sees confirmation receipt
- `pay.html` without params shows a demo invoice; with `?invoice=INV-XXXX` loads from database

## Current State

Demo mode — uses localStorage for storage. All pages work standalone.

## Production Roadmap

See `PAS_Security_Architecture_Guide.md` for full details on:
- Supabase database setup
- Stripe integration
- Webhook security
- WhatsApp/Twilio integration
- Data architecture

## File Structure

```
├── index.html          Landing page
├── pay.html            Client payment (demo + dynamic)
├── success.html        Payment confirmation
├── admin.html          Admin dashboard
├── assets/
│   └── PAS_LOGO.png    Logo file (add this)
└── README.md
```

---
Demo concept by Tyler Peller
