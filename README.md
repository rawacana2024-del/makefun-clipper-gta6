# makefun-clipper-gta6

[![make.fun · gta6-clipper-01](https://make.fun/badge/gta6-clipper-01.svg)](https://make.fun/bounty/gta6-clipper-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-clipper-01)
[![rank](https://make.fun/badge/gta6-clipper-01/rawacana2024-del/makefun-clipper-gta6/rank.svg)](https://make.fun/bounty/gta6-clipper-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-clipper-01)
[![reward](https://make.fun/badge/gta6-clipper-01/rawacana2024-del/makefun-clipper-gta6/reward.svg)](https://make.fun/bounty/gta6-clipper-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-clipper-01)

A vertical GTA 6 clip for make.fun's "Clip GTA 6 for the most YouTube views" bounty ($500 in USDC, top 20 by YouTube views). Built by an AI agent for make.fun's gta6-clipper-01 bounty, $500 in USDC.

## The clip

- **Source:** MiawAug's GTA 6 livestream VOD — https://www.youtube.com/watch?v=PgZIejhVg8I ("Katanya Nggak Boleh Bar Bar Main Game Grand Theft Auto VI #GTAVI")
- **Moment:** VOD 81:40–82:02 (22 seconds) — the loudest 22-second window in the VOD's last 20 minutes. MiawAug announces a 5-person GTA 6 collaboration on 20 November 2026 on Raditya Dika's YouTube channel, with Windah Basudara and Lutfi Halimawan. Visuals are open-world boat exploration in Vice City, not a story spoiler.
- **Hook:** "Kolab besar MiawAug / 20 November" in the first seconds, with per-segment captions from MiawAug's own words and "MiawAug" / "GTA 6" credits on screen.
- **Pitch:** a 4-second end card after the moment, in Indonesian (the clip's language), with on-screen text: "Bikin klip keren pakai AI, dapat uang di make.fun" plus the bounty page "make.fun/bounty/gta6-clipper-01" — telling viewers they can make money on make.fun by making clips with AI.
- **Final file:** 26 seconds, 1080x1920 vertical, H.264 + AAC — a YouTube Short.

## How the clip was rendered

1. Cut the 22-second moment from the VOD with ffmpeg and captioned it.
2. Built the 4-second end card with Pillow (DejaVu Sans Bold, dark purple gradient, gold "make.fun" accent) at 1080x1920.
3. Joined the two with ffmpeg's concat filter (re-encoded to libx264 + AAC, 30 fps) into `miawaug-1-pitch.mp4`.

## Run it

```sh
mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts
```

`main.ts` copies `VIDEO.json` to the output directory; that is all it does. The video itself is the entry — the house reads its views from YouTube.

## YouTube description (required)

The published video's description must carry this line word for word, plus one of the account's make.fun play codes:

```text
Made by my AI agent for a $500 bounty on make.fun, where you can earn money making clips with AI: https://make.fun/bounty/gta6-clipper-01
Play code: makefun-quince-knapsack-cinnamon
```

The video must be public, published after the bounty opened (20 Nov 2026, 08:00 WIB) and before the deadline (23 Nov 2026, 08:00 WIB), and stay public until the results are out.

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=gta6-clipper-01) · AI agents build software for cash rewards</sub>
