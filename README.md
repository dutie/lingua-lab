# lingua-lab

A self-hosted language learning system. Spanish + French (active), Japanese (ambient), Chinese (later).

## The stack

Two containers, one git repo.

- **Audiobookshelf** — serves podcasts to your phone for commutes. Download episodes on WiFi, play offline.
- **Tailscale** — private mesh network. Your phone reaches the server from anywhere by the name `lingua-lab`, no port forwarding, no public exposure.
- **Obsidian** — the vault lives in git. GitHub is the canonical copy. Your phone and desktop both pull/push via obsidian-git. No sync server required, works when your home server is off.

## Directory layout

```
lingua-lab/
├── docker-compose.yml
├── .env.example                 ← copy to .env, fill in Tailscale key
├── README.md                    ← you are here
├── PLAN.md                      ← the weekly regime
├── PODCASTS.md                  ← what to subscribe to in ABS
├── audiobookshelf/              ← server data (gitignored)
├── tailscale/                   ← tailscale state (gitignored)
└── vault/                       ← Obsidian vault (IS in git, open this folder in Obsidian)
    ├── Home.md                  ← dashboard — open Obsidian and this loads first
    ├── README.md                ← vault conventions
    ├── es/                      ← Spanish notes, SR-tagged
    ├── fr/                      ← French notes, SR-tagged
    ├── ja/                      ← Japanese notes, SR-tagged
    ├── hanzi-kanji/              ← cross-linguistic CJK character study (later)
    ├── concepts/                ← cross-language reference map (no SR)
    ├── inbox/                   ← quick capture from commutes, process in evening
    ├── templates/               ← copy-ready note formats
    └── resources/               ← curated external vaults and links
```

## First-time setup

### Server side (one-time, ~15 min)

1. Install Docker if you haven't. On WSL2: you already have it.
2. Get a Tailscale account at https://tailscale.com — free tier is fine forever.
3. Get an auth key: https://login.tailscale.com/admin/settings/keys → Generate → mark **Reusable**.
4. `cp .env.example .env` and paste your auth key.
5. `docker compose up -d`
6. Verify the container joined your tailnet: https://login.tailscale.com/admin/machines — you should see `lingua-lab`.

### Audiobookshelf bootstrap (5 min)

1. On your phone, install Tailscale, sign in, connect.
2. Open `http://lingua-lab:13378` on your phone (MagicDNS resolves the name).
3. Create admin account.
4. Libraries → Add Library → name **Podcasts**, type **Podcast**, folder `/podcasts`.
5. Add the six podcasts from `PODCASTS.md` via the UI (Find Podcast tab, search by name).
6. Install the ABS app on your phone, sign in. Episodes auto-download.

### Obsidian + git workflow (10 min)

The vault IS a git repo. You clone it on every device where you want Obsidian, and obsidian-git keeps the clones in sync via GitHub.

**On your desktop:**

1. Clone this repo somewhere permanent (e.g. `~/repos/lingua-lab`).
2. Open Obsidian → "Open folder as vault" → point at `lingua-lab/vault/`.
3. Community plugins → Browse → install and enable:
   - **Spaced Repetition** (by st3v3nmw)
   - **Obsidian Git** (by Vinzent03)
4. Obsidian Git settings → set auto-pull interval to 10 min, auto-push on file change, commit message template: `vault: {{date}}`.
5. Spaced Repetition settings:
   - Flashcard tag: `#sr`
   - Flashcard separator: `::`

**On your phone:**

1. Install Obsidian mobile.
2. Install `mGit` (Android) or use Working Copy (iOS) to clone the repo to a local folder first — Obsidian mobile can't clone, it can only open an existing folder.
3. In Obsidian, open that folder as a vault.
4. Install the same two plugins. Same settings.

First time the app opens, it pulls the latest from GitHub. When you write a note, it auto-commits and pushes. Conflicts are rare since most of your edits happen during different slots of the day, but when they do occur obsidian-git prompts you to resolve — don't panic, it's a markdown merge.

## The plan in one paragraph

Weeks 1–6: **Spanish and French alternate by day** (Mon/Wed/Fri Spanish, Tue/Thu French) to minimize cross-linguistic interference. Japanese stays as ambient listening on your 17:00 break, no active study. Chinese deferred to week 13+. Full schedule and switchover criteria in `PLAN.md`.

## What this is not

- A Pinchflat/YouTube pipeline. Real learning podcasts have RSS.
- A universal concept SR system. Cross-language cards train translation-mediated retrieval. `concepts/` is navigation only, never tagged `#sr`.
- A Whisper transcription stack. You don't have time to study transcripts you're not already listening to.
- A zero-touch deploy. You still have to *do the work* — subscribe, review, write cards, show up on Monday morning.
