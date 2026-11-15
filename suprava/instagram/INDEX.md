# Suprava Sabat (@suprava.ss) — Instagram corpus — INDEX

Built 2026-11-12. Local corpus only, from `~/workspace/ig/` (read-only source; nothing under `~/workspace/ig/` was modified).
Main file: `suprava.ss-merged.txt` — one section per post, sorted by `taken_at_iso` ascending, verbatim content only (captions, reel transcripts, OCR text). Nothing summarized or paraphrased in the merged file.

## Verified counts

| Item | Count |
|---|---|
| Posts in `data/posts/suprava.ss.jsonl` | **162** |
| — kind `clips` (reels) | 90 |
| — kind `carousel_container` | 57 |
| — kind `feed` (single image) | 15 |
| Date range (taken_at_iso) | **2023-08-29 → 2026-10-03** |
| Total likes (all 162 posts) | 897,006 |
| Total comments (all 162 posts) | 84,924 |
| Posts with empty caption | 0 |
| Reel transcript files present (`data/transcripts/suprava.ss/`, 90 .txt) | **90 of 162 posts** |
| — of which real transcripts | 70 (45 long + 25 short-but-real, e.g. music lyrics: "Music.", "Yeah.", "My heart longs for you.") |
| — of which NO-SPEECH music reels (marker `[No speech — music-only reel...]`, added 2026-11-15) | **10** — the last 429 placeholders, resolved 2026-11-15: Qwen demo still throttling (0/10 retried, then probe returned `响应结构不完整`), so local faster-whisper base (validated: near-exact match to Qwen ground truth on `DEwa4j0Cwwb`) transcribed all 10 and found NO intelligible speech in any of them (control: same model returns misheard-but-non-empty text on song-with-vocals reels). All 10 are loud music (-6 to -16 dB mean) with text-overlay captions — instrumental background music, no speech to transcribe. |
| — of which ERROR PLACEHOLDERS (Chinese Qwen rate-limit text `请求失败 (状态码: 429): Workspace requests rate limit exceeded`) | **0** (resolved 2026-11-15, see row above) |
| — of which NO-AUDIO videos (`.mp4` files with zero audio streams, verified by ffprobe — silent/text-on-screen reels, nothing to transcribe) | **10** |
| Posts with NO transcript file | **72** (mostly carousels / image posts, which have no audio) |
| OCR files present | **467 .txt files, covering 69 posts** — 399 MiniCPM (hcnsec, `data/ocr_hcnsec/suprava.ss/`, 52 posts) + 68 RapidOCR local (`data/ocr_rapidocr/suprava.ss/`, added 2026-11-15 for the 17 posts that had images but no OCR; validated against hcnsec ground truth on 3 images and cross-checked vs tesseract 5.3.4 on 3 more — comparable quality, occasional joined words like `ForB2BCompanies`). All real OCR text; `DZ67Omfkeh1_4.txt` was misflagged as a placeholder in v1 — its content is genuine slide OCR about Reddit DM limits. |
| Audio files (`audio/suprava.ss/`) — counted only, NOT copied | **90 files: 80 .m4a (21,736,592 bytes) + 10 .mp4 (31,317,888 bytes) = 53,054,480 bytes total** |
| Image files (`data/images/suprava.ss/`) — counted only, NOT copied | **557 files, 209,664,314 bytes total** |
| Transcript files not matching any post in the jsonl | 0 |
| OCR codes not matching any post in the jsonl | 0 |

### Merged file verification (on disk)

- File: `suprava.ss-merged.txt` (v4, rebuilt 2026-11-15 — v1 kept as `suprava.ss-merged.v1.txt`; rebuild script: `../rebuild_merged.py`, now reads both OCR dirs and counts no-speech markers separately)
- Lines: **11,249** (`wc -l`)
- Words: **49,236** (`wc -w`)
- Bytes: **350,319** (`wc -c`)
- First section: post `Cwha77XyFTr`, 2023-08-29 (caption about B2B lead generation, DM "LINKEDIN")
- Last section: latest post in range, 2026-10-03
- Missing transcript / missing OCR are marked in the file as `[NO TRANSCRIPT FILE]` / `[NO OCR FILES FOR THIS POST]`; the 10 no-speech music reels carry their `[No speech — music-only reel...]` marker, and the 10 silent videos `[NO AUDIO — video file has no audio stream, ASR not applicable:]`, counted separately above. **Zero 429 placeholders remain.**

## Recurring topics (factual, from reading the merged content)

Top hashtags across all 162 captions: #leadgeneration (75), #sales (60), #ai (60), #business (45), #b2b (44), #coldemail (43), #leads (41), #marketing (40), #leadgen (39), #unitedstates (31), #entrepreneur (18), #smma (15).

Phrase counts in the merged file (captions + transcripts + OCR): AI 1,074 · sales 183 · LinkedIn 113 · cold email 101 · B2B 89 · DM 93 · agency 69 · lead generation 56 · automation 22 · playbook 18 · Apollo 14 · cold outreach 14 · Sales Navigator 7.

Recurring topics (short factual list):
- B2B lead generation (core topic)
- Cold email / cold outreach (scripts, deliverability, sending)
- LinkedIn outreach and lead scraping (Sales Navigator, Apollo)
- AI tools for sales / AI agents / AI workflows (incl. Claude, GPT)
- Sales psychology and closing / client acquisition for agencies (SMMA)
- Scraping / data enrichment for leads
- Free tools, templates, workflows and playbooks as lead magnets

## Links / products / CTAs mentioned in captions

- **No URLs at all appear in any caption** (0 `http` links found across all 162 captions).
- CTAs are comment/DM-keyword based, not links. "Comment" appears in 49 captions, "comment" (lowercase) in 37, "DM" in 32, "free" in 30.
- Comment keywords used (caption text): "email" (5), "send" (4), "leads" (3), "skills" (2), "workflow" (2), "agent" (2), "AI" (2), "access" (1), "podcast" (1), "yes" (1), "banned" (1), "GTM" (1), "Claude" (1), "github" (1), "LinkedIn" (1), "hormozi" (1), "tools" (1), "tool link" (1), "GPT" (1), "cold email" (1).
- DM keywords used: "LEADS" (1), "LINKEDIN" (1); "DM me" appears in 2 captions.
- "link in bio" / "Link in bio" appears in 5 captions.
- Lead magnets named in captions: a **lead-generation playbook** (comment "access" and she DMs the playbook — 4–5 captions mention "playbook"); free tools / templates / workflows / AI agents sent by DM.
- No priced product, course link, or external store link is named in any caption.

## Mentions by others

Grep of the WHOLE transcript corpus (`data/transcripts/*/*.txt`, case-insensitive "suprava"):
**Zero hits in any other account's reel speech.** BUT she IS named in another account's caption: **@leadgenman**, post `DO5aqMEDm5m` (2025-09-22, "9 out of 10 outbound teams are still doing manual research…"), lists her under "TOP VOICES IN AI SALES TO FOLLOW: … Suprava Sabat …" (caption in `data/posts/leadgenman.jsonl`).

## Notes / gaps

- **Retranscription rounds 2026-11-12** (`~/workspace/ig/bin/redo_suprava.py`, Qwen ASR demo, WORKERS=4): of the original 47 placeholders + 10 missing transcripts, **37 recovered as real speech** (70 real transcripts now, up from 33). **10 remained 429 placeholders** — the demo throttles again after ~10 successes per round. **Resolved 2026-11-15 (0 placeholders left):** Qwen demo re-probed and still failing (`响应结构不完整`, 0/10 on the retry), so local faster-whisper base (int8, in `~/workspace/ig/venv-asr/`, av pinned 12.0.0) transcribed all 10 — validated first against Qwen ground truth on `DEwa4j0Cwwb` (near-exact) — and found **no intelligible speech in any of the 10**; they are music-only reels (loud audio, text-overlay captions), now marked `[No speech — music-only reel...]` instead of placeholders. Also fixed in the script: it used to reject any result under 10 characters as "too short" — but genuine music-lyric reels return things like "Music." / "Yeah." / "Ah.", so the threshold now accepts any non-empty, non-error result. **10 are un-transcribable by nature**: their `.mp4` files contain no audio stream at all (ffprobe-verified), silent/text-on-screen reels whose words live in OCR, not audio.
- 72 posts have no transcript file at all (mostly carousels / image posts, which have no audio).
- OCR covers **69 posts (467 files)** — 399 hcnsec MiniCPM + 68 local RapidOCR (added 2026-11-15 for the 17 image posts that had no OCR). OCR text quality varies (fragmented slide text, some garbled; RapidOCR occasionally joins words).
- Media files (audio/images) were NOT copied into this folder — only counted. They remain under `~/workspace/ig/audio/suprava.ss/` and `~/workspace/ig/data/images/suprava.ss/`.
