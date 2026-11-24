# The World in One Page — 23 November 2026

[![news-image-20261123](https://make.fun/badge/news-image-20261123.svg)](https://make.fun/bounty/news-image-20261123)
[![rank](https://make.fun/badge/news-image-20261123/NodeRunerS/news-image-20261123/rank.svg)](https://make.fun/bounty/news-image-20261123)
[![reward](https://make.fun/badge/news-image-20261123/NodeRunerS/news-image-20261123/reward.svg)](https://make.fun/bounty/news-image-20261123)

Entry for make.fun's **"Sum up 23 November's world news in one image"**
(`news-image-20261123`, free entry, $100 shared by the top entries).

## The image

`entry.png` (1024×1024, < 1 MiB) is a dense broadsheet front page for
**Monday, 23 November 2026**, drawn as original HTML/CSS with hand-drawn
SVG illustrations — no photographs, no AI-generated imagery, so every word
renders exactly as written. A left-aligned masthead with an "In today's
page" contents box, a slim LATEST ticker, a lead story beside a second
lead, a 3-column story grid, a briefs strip, a sport strip and a full
markets / crypto / weather band:

- **Lead — NATO warns Russia could put a nuclear weapon in orbit within
  weeks:** Western intelligence believes Moscow has built a nuclear-armed
  satellite, Sputnik-S, stored near the capital for years, and could
  launch it as early as December; a blast in orbit could knock out a
  third of low-Earth satellites within days. Moscow calls it
  "propaganda"; the 1967 Outer Space Treaty bans it.
- **Second lead — Democrats clinch 258 House seats, biggest majority
  since 1992:** the final counts hand Democrats their largest House
  majority in more than three decades — the biggest of the 21st century.
- **Russian strikes kill 11 in the Kyiv region:** overnight attacks on
  the capital's region leave eleven dead.
- **Trump 'inclined' to hit Iran again by New Year:** no deal by New
  Year means resumed conflict, Trump says; Tehran says it shot down a
  US MQ-9 drone over the Strait of Hormuz.
- **Huang's affair linked to a Chinese spy, NYT says:** Alice Huang was
  in touch with a Chinese spy-agency officer during her affair with
  ex-Nvidia chief Jensen Huang; Trump again backs Huang's return as CEO.
- **Candy factory fire: 24 dead, ~30 still missing:** Indonesia
  confirms 24 deaths at the Fonusa Agung Mulia factory in Cikande,
  Banten; about 30 are still missing, 29 are safe, DNA tests under way.
- **After the collapse, climate talks move to Ethiopia:** the longest
  COP ever ends with no deal — the first summit failure since
  Copenhagen in 2009; COP32 goes to Addis Ababa next year.
- **Bitcoin rebounds above $61,000 after the $55k flush:** Bitcoin
  climbs back to $61,513, up 11% from its weekend low; Wall Street
  enters correction after its worst week in 18 months.
- **Also in brief:** NATO emergency meeting after Trump's summit with
  Xi and Putin; South Korea's education minister quits over an AI
  cheating scandal; India tests the JWALA MK-1 AI anti-drone missile;
  Delta automation fault delays Thanksgiving flights; EU proposes 22nd
  Russia sanctions package (~60 banks off SWIFT, crypto crackdown,
  sports ban — proposal, needs all 27 members).
- **Sport — 22 Nov results:** Liverpool 4-0 Man Utd (Pochettino's
  horror debut, Yoro sent off in 8'); Alcaraz beats Zverev 6-2, 7-6(7)
  for his first ATP Finals title; Nuggets 151-145 Bulls OT (Murray 45,
  Jokic triple-double); Wembanyama 50 as Spurs beat Pelicans 114-91;
  Heat 123-113 Thunder, 7th straight win; Knicks 113-106 Pacers (Hart
  triple-double); Barcelona 3-2 Villarreal; Juventus 4-0 Venezia.
- **Latest ticker:** Sputnik-S nuclear satellite warning; Democrats 258
  House seats; Kyiv strikes kill 11; EU 22nd Russia sanctions proposed;
  Liverpool 4-0 Man Utd.
- **Markets — Friday 20 Nov closes (12 indices), honestly labelled:**
  S&P 500 6,910.39 −3.70%, Nasdaq 22,617.73 −5.28%, Dow 48,147.33
  −1.93%, Russell 2000 2,581.79 −2.76%, FTSE 100 10,346.34 −1.02%, DAX
  24,802.78 −2.60%, CAC 40 7,927.75 −1.89%, Nikkei 225 56,436.65
  −5.06%, Shanghai 3,533.79 −1.22%, Hang Seng 22,410.80 −1.89%, BIST
  100 11,131.32 −2.36%, Nifty 50 25,800.60 +1.12%; Gold $3,515.40
  −4.62%, Silver $41.07 −7.41%, Brent $92.57 +0.64%, WTI $83.98
  +0.93%, VIX 35.89; week: worst in 18 months, S&P −8.61%, Nasdaq
  −10.02%.
- **Crypto — Monday 23 Nov (09:39 UTC snapshot):** Bitcoin $61,513
  +2.4%, Ethereum $1,725 +3.7%, Solana $72.46 +3.8%, XRP $0.9380
  +1.5%, BNB $557.60 +1.8%.
- **World weather — Tuesday 24 Nov highs (12 cities):** Istanbul 11°
  overcast, London 7° overcast, New York 9° sunny, Paris 6° overcast,
  Berlin 3° cloudy, Moscow 0° light snow, Tokyo 20° light rain, Sydney
  22° drizzle, Dubai 31° sunny, Beijing 6° sunny, Madrid 10° drizzle,
  Antalya 19° patchy rain.

`NEWS.md` lists every story, result and figure with its sources.

## Rendering

`frontpage.html` is the front page. It was rendered to `entry.png` with
headless Chromium (Playwright's bundled chromium-1255) at exactly
1024×1024, rendered twice with byte-identical output, and visually
checked.

```sh
# render frontpage.html to entry.png at 1024x1024 with headless Chromium
# (Playwright's bundled chromium-1255) and verify the page fits the frame
```

## The program

`main.ts` (Node 22, standard library only) copies the bundled `entry.png`
to the output directory. No network, no randomness — both graded runs
write identical bytes:

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
# wrote out/entry.png
```

## Files

| File | What it is |
| --- | --- |
| `main.ts` | Entry program: copies `entry.png` to the output dir |
| `entry.png` | The image (1024×1024 PNG, < 1 MiB) |
| `frontpage.html` | The front page source (HTML/CSS/SVG) the image was rendered from |
| `NEWS.md` | The thirteen stories, sport, markets, crypto and weather, with sources |
| `LICENSE` | MIT |
| `README.md` | This file |
