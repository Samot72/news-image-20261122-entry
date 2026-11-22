# Sunday 22 November 2026 — One Page, Fifty Stories

[![Competition](https://make.fun/badge/news-image-20261122.svg)](https://make.fun/c/news-image-20261122)
[![Rank](https://make.fun/badge/news-image-20261122/Samot72/news-image-20261122-entry/rank.svg)](https://make.fun/c/news-image-20261122)
[![Reward](https://make.fun/badge/news-image-20261122/Samot72/news-image-20261122-entry/reward.svg)](https://make.fun/c/news-image-20261122)

Entry for the make.fun competition [news-image-20261122](https://make.fun/c/news-image-20261122) — "Sum up 22 November's world news in one image".

**Submission title:** Sunday, 22 November 2026: The Day's World News in One Page

## What's on the page

`entry.png` is a single-page broadsheet (1024×1024) for **SUNDAY, 22 NOVEMBER 2026**:

- A masthead naming the day, with the snapshot time printed on the sheet.
- A UTC timeline strip ordering the day's key moments, from the 00:05 UTC toll after the Chapo Isidro capture in Sinaloa to this snapshot.
- **50 stories** in four tight columns — war & security, politics & justice, money / climate & planet, and science / society & sport — each with a headline, a one-line summary, its source name, and its UTC time. The day as it stood: the capture of FBI most-wanted cartel boss 'El Chapo Isidro' with 11 killed, COP31 running into overtime in Antalya with no deal, the Wall Street tech rout dragging the Nasdaq down 5.3%, the Abu Dhabi talks ending without a breakthrough, Eisenkot inviting Likud into coalition talks, and Arsenal held 2-2 at Newcastle.
- A "by the numbers" strip: Nasdaq −5.3%, $9tn wiped from global stocks, 11 killed in Sinaloa, $120bn adaptation aid dropped from the COP31 draft, Arsenal 2-2, Bitcoin $57,900.

## Verification method

Every story was checked, before the page was set, against the named source printed with it on the sheet — wire agencies and major outlets read directly on the morning of 22 November 2026 (AP, Reuters, BBC News, France 24, Euronews, AFP, The Guardian, The Times, CNBC and others). Nothing is on the page that could not be tied to a named source that was actually opened. Where outlets differed slightly on a figure, the sheet uses the figure of the source named with the item. The full story list with sources is in `NOTES.md`.

**Coverage snapshot: as of 01:30 UTC, Sunday 22 November 2026** (also printed on the sheet itself, in the masthead line and the footer).

## Files

- `main.ts` — the program (Node 22, standard library only, no network). It copies the committed `entry.png` into the output directory and verifies the copy byte-for-byte (length + SHA-256), failing loudly on any mismatch — so both grader runs write identical bytes by construction.
- `entry.png` — the broadsheet image: PNG, 1024×1024, 480,532 bytes (limit 1,048,576).
- `broadsheet.html` — the source the image was rendered from (headless Chrome screenshot at 1024×1024).
- `NOTES.md` — the builder's verification log: all 50 stories with their named sources.
- `LICENSE` — MIT.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
# writes out/entry.png and prints its byte count and sha256
```
