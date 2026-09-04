# Jaano — GFF 2026 Panel Loop

> **THE DELIVERABLE: `jaano-gff-portrait.html`** — 33.0 s, 5 scenes, seamless loop
> (re-cut 2026-08-31: ends on the booth-number close, slower pacing, bigger journey
> phone, Blostem "FROM THE HOUSE OF" masthead on the close).
> **`Jaano-GFF-Portrait-33s.mp4`** = the same cut as a video (1080×1920, 30 fps,
> exactly 33.000 s, cut wipe-cover → wipe-cover so it loops seamlessly — play it on
> repeat). `Jaano-GFF-Loop-60s.mp4` is **OUTDATED** — the old 9-scene 60 s landscape cut.
>
> `jaano-gff-portrait.html` = the same loop as a live HTML page (source of truth —
> edit `src/jaano-gff-portrait.html`, rebuild, re-record to refresh the video).
> `jaano-gff-loop.html` = the earlier LANDSCAPE 16:9 cut (kept in case the screen
> is horizontal). Video re-render pipeline: record ≥2 full cycles with Playwright
> (`recordVideo`, `channel:'chromium'` — headless runs the page ~25 % slow, that's
> expected), find the loop-wrap wipe-COVER frames (uniform violet frame right after
> the CLOSE scene — the REC HUD rolling back to 00:00 marks the wrap; other wipes
> look identical), trim cover→cover with **input-side** `-ss`/`-t`, then
> `setpts`-normalize that span to exactly 33.0 s, `fps=30`, encode libx264 crf 18
> (ffmpeg via `imageio_ffmpeg.get_ffmpeg_exe()`).

A self-running, seamlessly looping animated deck (30 s portrait cycle; the landscape
16:9 cut still runs the older ~92 s program) for the booth panel at
Global Fintech Fest 2026 (Booth J18 & J20, Jio World Centre). Maison Blanc art direction
(Bodoni Moda display, violet→blue metal gradient, जानो ghost) with real product screens
and the AI persona imagery from the GFF landing's three-model switcher.

## Files

| File | What it is |
|---|---|
| `jaano-gff-loop.html` | **The deliverable.** Single portable file — fonts + images inlined (~1 MB). Copy to the booth machine, double-click, press `F`. Works fully offline. |
| `src/jaano-gff-loop.html` | Editable working source (references `../fonts.css` + `../img/`). |
| `fonts.css` | Bodoni Moda (roman+italic), Lato 900, Caveat — woff2 data URIs (from the GFF landing). |
| `img/` | Customer-journey phone mocks (webp), console screenshots (vpd-*), AI persona crops (call-tile / avatar / phone / officer-pip). |

> Note: macOS's filesystem is case-insensitive — never keep `Jaano-GFF-Loop.html` and
> `jaano-gff-loop.html` in the same folder; they are the same file. That's why the source
> lives in `src/`.

## Playing it at the booth

- Open in Chrome → press **F** for fullscreen. The stage is a fixed 1920×1080 canvas that
  auto-scales to any panel resolution (letterboxed if the panel isn't 16:9).
- **Space** pause/resume · **← →** jump scenes (handy when talking someone through it) ·
  cursor auto-hides after ~2.5 s.
- Fully offline — no fonts, images or scripts fetched from the network.
- Chrome kiosk autostart: `chrome --kiosk --autoplay-policy=no-user-gesture-required file:///path/to/Jaano-GFF-Loop.html`

## The 11 scenes (~92 s)

1. **Hook** (5.0 s) — "Anyone can look good ~~on paper~~." + Caveat payoff line
2. **Title** (4.8 s) — जानो dictionary entry → metal *Jaano* + the three senses
3. **Meet Rahul** (4.8 s) — intro: "Rahul wants a loan." + context ("New city… His bank sends one link.")
4. **The journey** (12.2 s) — near-fullscreen phone (830 px) flips the 8-step flow at 1.4 s/step,
   with floating command pills, a stepped progress bar, a scan sweep and ken-burns push-in per screen
5. **Close** (6.2 s) — "Jaano knows." + BOOTH J18 & J20 + FROM THE HOUSE OF **Blostem** → loops

Dropped from the old cut: interview tile, APPROVED stamp, any-language, three-ways,
beyond-banks (sections removed from `src/jaano-gff-portrait.html`; their CSS remains, harmless).
