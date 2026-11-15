# Instagram Reels Texts — clean extracted texts

Clean, real extracted texts from **238 Instagram accounts** — speech transcripts of reels/videos and OCR text of carousel/feed images.

## Contents (verified counts, built 2026-11-15)

| Folder | Files | Size | What it is |
|---|---|---|---|
| `transcripts/` | 45,104 | 44.5 MB | Real speech transcripts, one file per post (`<user>/<post_code>.txt`) |
| `ocr/` | 27,017 | 7.8 MB | OCR text of carousel/feed images, one file per image (`<user>/<post_code>_<idx>.txt`) |
| **Total** | **72,121** | **52.3 MB** | |

See `counts.json` for the machine-readable counts.

## What is NOT in this repo (excluded on purpose)

- **Qwen error placeholders** — ~14,224 transcript files that only contain a rate-limit / API error text (`429` / `400` / `请求失败`). Those files are being repaired locally with Whisper and will be added here as they become real.
- **Empty files** — none in the corpus.
- **`[No speech]` / `[No audio]` marker files** — verified verdicts (music-only reels, silent clips), not speech text.

## Method

- **Audio → text:** local faster-whisper (base model, int8), language auto-detected (mixed English / Arabic, incl. Egyptian dialect). Earlier files were transcribed with Qwen ASR; files whose Qwen output was an error placeholder were re-transcribed locally.
- **Images → text:** hcnsec MiniCPM OCR, plus local RapidOCR for images the first engine missed.
- **Quality:** English transcripts are near-exact; Egyptian-Arabic transcripts can contain word errors but the meaning is recoverable. OCR can contain joined words on dense slides.

## Structure

```
transcripts/<instagram_username>/<post_code>.txt   # one file per video post
ocr/<instagram_username>/<post_code>_<idx>.txt    # one file per image
counts.json                                       # verified counts for this snapshot
```

`<post_code>` is the Instagram shortcode from the post URL (`instagram.com/reel/<post_code>/`).

## Status

This is a **snapshot**: the local repair of the remaining ~14,224 error transcripts is still running, and this repo is updated as more files become clean. The counts in `counts.json` describe exactly the files in this commit — nothing more.

## Note

These are transcriptions/OCR of public Instagram posts, published for research and personal study. If you are a creator whose content appears here and you want it removed, open an issue.
