# Jaano — GFF 2026 Booth Panel Loop · Handoff

**What this is:** a self-running, seamlessly looping animated presentation for the
Jaano panel at Global Fintech Fest 2026 (Booth J18 & J20, Jio World Centre, Mumbai,
9–11 Sep). Portrait 1080×1920, ~45 s per cycle, zero technical jargon — built to stop
a passer-by mid-walk.

---

## The deliverables (all in `~/Downloads/jaano-gff-loop/`)

| File | Use it when |
|---|---|
| **`jaano-gff-portrait.html`** | **The deliverable.** The full loop as a single offline page — fonts and images embedded, nothing loads from the network. Open in Chrome → press **F** for fullscreen. Space = pause, ←/→ = jump scenes, cursor auto-hides. |
| `jaano-gff-loop.html` | Older **landscape 16:9** cut (different, longer program). Only if the screen turns out horizontal. |
| `src/jaano-gff-portrait.html` | The editable source, for future changes. Rebuild the single file after edits (inline `fonts.css` + `clash.css` + `img/`). |
| `fonts.css`, `clash.css`, `img/` | Assets the source links to (fonts, journey phone mocks, the AI face screen, Jaano mark, Blostem logo). |

**Making the video file:** screen-record the HTML playing fullscreen (QuickTime → New
Screen Recording), capture at least one full ~45 s cycle, and trim both ends to the violet
scene-wipe — that makes the file loop seamlessly on any panel player.

---

## The program (~45 s, 6 scenes, violet wipe between each)

1. **Hook (5.0 s)** — *"Anyone can look good ~~on paper~~."* word-slams in with a red
   strike, then the handwritten payoff: *"Meeting them is a different story."*
2. **The name (4.8 s)** — big metal **Jaano** + scrawl underline → *"it means 'to know'"*
   → the three senses: to verify — check the papers · to understand — hear the story ·
   to trust — know the person.
3. **Meet Shreya (4.8 s)** — *"Shreya wants a loan."* New city, new job, nearest branch
   40 km away → *"Her bank sends one link."*
4. **The journey (12.8 s)** — a large phone runs the real 7-step flow (tap the link →
   allow camera → read the code aloud → show PAN → flip to Aadhaar → blink twice on the
   live face-check screen → sign & show), each step titled by a big instruction pill
   above the phone, with a scanner line sweeping the screen. After a beat on the last
   step, a violet **VKYC · VERIFIED** seal slaps onto the phone with an impact shake —
   then **"Under 3 minutes." — FROM HER SOFA · NO BRANCH · NO APP**.
5. **Three ways to meet (10.2 s)** — the three models as stacked cards, a violet
   spotlight ring hopping down them: **01 With an officer** (live video interview) ·
   **02 By yourself** (guided, on your phone) · **03 With the AI guide** (in your
   language) → **SAME TRUST · YOUR CHOICE**.
6. **Close (7.4 s)** — *"Anyone can verify. **Jaano knows.**"* + scrawl → then, word by
   word, **देखो · सुनो · जानो** (Rozha One; dekho/suno in soft grey, jaano in brand ink)
   → **VERIFY · UNDERSTAND · TRUST** → **POWERED BY Blostem**. The ghost जानो watermark
   grounds the bottom edge. Loops back to the hook.

A persistent **Jaano fingerprint-mark + JAANO** chrome (top-left) and a gradient
progress hairline (bottom) run through the whole loop.

---

## Booth-day checklist

- [ ] Confirm the panel's **orientation** (this cut is portrait 9:16) and whether it
      plays **MP4 or a browser** — record the video from the HTML if it needs a file.
- [ ] Set the player to **loop/repeat**; the cycle is built to repeat invisibly.
- [ ] If HTML: Chrome, press **F**, plug in power, disable sleep
      (`chrome --kiosk file:///…/jaano-gff-portrait.html` for unattended start).
- [ ] Audio: the loop is silent by design (exhibition halls drown audio anyway).
- [ ] Test from ~4 m away — all copy was sized for hallway legibility.

## Asset provenance (if anyone asks)

Journey phone screens are the designed Jaano mock series; the live face-check screen is
an AI-generated persona; the fingerprint-J mark and Blostem logo come from the GFF
landing site; fonts are OFL/free (Clash Display, Lato, Inter, Rozha One, Baloo 2)
embedded in the file — nothing loads from the network, nothing licensed.

*Maintained by Anhad · last updated 1 Sep 2026.*
