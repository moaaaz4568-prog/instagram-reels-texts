# Suprava Sabat — collected public posts

Everything Suprava Sabat (founder/co-founder of AcquisitionX, B2B lead-gen agency, Bangalore) has published publicly, collected 2026-11-12 with a completion pass 2026-11-15.

- Instagram: [@suprava.ss](https://www.instagram.com/suprava.ss/) — `instagram/`
- X: [@Suprva02](https://x.com/Suprva02) — `x/`
- LinkedIn: [suprava-sabat-saasleadgen](https://www.linkedin.com/in/suprava-sabat-saasleadgen/) — `linkedin/`
- YouTube: no own channel — guest appearances only — `youtube/`

## Contents

| Folder | Files | What it is |
|---|---|---|
| `instagram/` | `suprava.ss-merged.txt` (11,249 lines, 162 posts), `INDEX.md`, `_build_stats.json` | All 162 posts 2023-08-29 → 2026-10-03: captions + speech transcripts (70 real, 10 music-only, 10 no-audio) + OCR of carousel/feed images. The per-post files also live in this repo under `transcripts/suprava.ss/` and `ocr/suprava.ss/`. |
| `x/` | `tweets.json` (401 originals), `replies.json` (1,391 replies), `suprava.tweets-merged.txt` (18,132 lines), `live_user_20261115.json` | 1,792 of 1,818 live tweets (98.6%), 2023-04-13 → 2026-11-13. |
| `linkedin/` | `posts.json` (810 items: 688 own + 122 reshares), `suprava.posts-merged.txt` (30,616 lines) | Complete as of 2026-11-11 — verified: no newer posts exist. Own posts 2020-11-24 → 2026-11-11. |
| `youtube/` | `README.md` only | No transcripts — see the note there. |

## Known gaps (honest, not hidden)

- **X: 26 tweets (1.4%) unrecoverable** — the API never serves them; their ids are unknown, so only a logged-in browser thread walk could find them.
- **X: 5 tweets truncated by X itself** (text ends "…", no full text in any API response) — needs a logged-in browser with "Show more".
- **X: 2 long-form article bodies unfetched** (only their promo tweets are here).
- **LinkedIn: complete.** Verified 2026-11-15 via the live activity page.

## Sources

- Instagram: local downloads + faster-whisper ASR + MiniCPM/RapidOCR.
- X: X GraphQL (UserTweets + UserRepliesTimeline), collected with the collector's own session.
- LinkedIn: LinkedIn Voyager API (memberShareFeed).
- No credentials, cookies or tokens are included anywhere in this folder.
