---
format: 1080x1080
duration: 70s
message: "Your statements go in. The whole model comes out."
arc: Hook → The work → Drop it in → Read it → Decide it → The memo → Brand
audience: Senior FP&A and corporate finance professionals
mode: collaborative
music: none
---

## Video direction

**Palette system** — from `frame.md`, dark register only, one register for the whole film.
Ground `ink-black` · text `cream` · secondary `cream-muted` · chrome + hairlines `cream-hint` /
`border-dark` · **`fire-orange` is the only accent in the entire video** and it marks exactly three
things: the payoff line of a statement, a load-bearing number, and the active segment of the pillar
rail. Red and mint appear **only inside captured product screenshots** (the `Reject` verdict, the
`RED FLAG` pills, green deltas) — they are the product's own colors, never promoted to a frame
accent. No second accent, no gradient ground, no shadow, no radius.

**Motion grammar + reveal model** — this film has **no voiceover**, so reveals are paced to
**reading time** instead: a line gets on screen for as long as a senior reader needs to take it in
(~0.35s per word, floor 1.2s), and the next piece does not arrive until the previous one has been
readable. The anti-front-loading discipline is unchanged — at t=0 show only the frame's first beat,
and spread the remaining reveals across the shot, especially the back half. Long-tail eases
(`power3` default); moves are **hard and precise, never bouncy** — no overshoot, no spring wobble,
no elastic. Typographic beats hard-cut; product screens seat and hold.

**Rhythm / held-frame allocation** — the film alternates dense and still on purpose:
frames **02, 05 and 06** are the dense ones (cascades, three stations, row-by-row findings);
frames **01, 04 and 07** carry real held reads. Frame **07's last 2 seconds are completely still** —
no jitter, no drift. After 60 seconds of density, stillness is the sign-off. During any hold, the
only sanctioned aliveness is a low-amplitude jitter on a single held element; no card breathing, no
lazy back-half pan.

**Bottom-band discipline** — captions are off (silent film) but the bottom ~17% of the canvas stays
clear of load-bearing content for bottom-edge consistency. Headlines, numbers and findings rows sit
in the top ~83%; only thin mono chrome (kickers, the meta line) may ride below it.

**Numbers rule** — every figure on screen is real output from the terminal's demo company. Nothing
is invented, rounded for effect, or presented as a benchmark. Wherever Halcyon figures appear the
`Sample data` chip stays legible.

**Screenshot-overlay doctrine (load-bearing — read before building any product frame).** The
captured screens in `assets/` are **static PNGs**. Nothing inside a PNG can animate. Wherever a
Scene line calls for internal movement — a KPI counting up, a slot border snapping amber, a scenario
toggle switching, a findings row sliding in — the screenshot stays the base layer and **only the one
component that moves is rebuilt in HTML and positioned over it at measured coordinates**, matching
the screenshot's own type, color and metrics so the seam is invisible. Do not rebuild the whole page,
and do not fake motion by cross-fading two screenshots. Where a region is rebuilt, the underlying
PNG region must be covered opaquely by the overlay so the static original never shows through behind
the live one. Screens were captured at 1920×1080 @2x; the frame canvas is 1080×1080, so every screen
is scaled and cropped to its region of interest — state the crop, don't letterbox.

**Negative list** — no stock photography · no purple-blue "AI" gradients or bokeh · no browser
chrome, nav bars, scrollbars or real cursors outside the deliberate UI beat in frame 03 · no
decorative shapes standing in for a real asset · no uppercase display type, no italic · no second
accent color · **no slideshow failure** (everything dumped by 25% then frozen) and **no screensaver
failure** (independent elements drifting with nothing leading).

## Frame 1 — Statements in, model out
- src: compositions/frames/01-statements-in-model-out.html

- scene: The thesis builds in three hard type beats on near-black, amber landing the payoff
- duration: 8s
- transition_in: cut
- status: animated
- type: hook
- persuasion: Value claim up front
- beat: assertion
- blueprint: kinetic-type-beats (Reproduce)
- focal: none (pure type)
- roles: none

Open cold on the promise, in their language. No product, no UI, no logo yet. The hook earns the
next 60 seconds by stating the trade the viewer actually cares about. Numbers stay out of beat 1 —
stakes first, evidence later.

Scene 1 (0.0–2.4s): ink-black ground, empty. The mono kicker `ANALYZE · MODEL · VALUE · COMMUNICATE`
types on at top-left and the catalogue numeral `01` sits top-right. Beat one — `three statements in.`
— hard-cuts in at display scale, lowercase, left-anchored on the upper third. Nothing else on screen.
Centered-left composition, ~55% empty.

Scene 2 (2.4–4.6s): beat one drops to 30% opacity in place (no move, no fade-out) and beat two —
`one integrated model out.` — **hard-cuts** in beneath it at full display weight. The swap itself is
the beat. Layout unchanged; the stack now occupies the middle third.

Scene 3 (4.6–6.6s): the amber rule stub wipes left-to-right, then the payoff `the whole fp&a loop. /
one terminal.` reveals **per word** in `fire-orange` at h2 scale. First amber of the film. The two
earlier beats hold at their reduced opacity — the frame now reads as a three-step argument.

Scene 4 (6.6–8.0s): fully resolved, held still. No camera, no drift. The held read sets the film's
baseline rhythm before the density of frame 02.

- handoff_out: none (clean hard cut into Frame 2)

## Frame 2 — What that normally costs
- src: compositions/frames/02-what-that-costs.html

- scene: The real file names and row counts stack up, then the task list cascades past faster than it can be read
- duration: 10s
- transition_in: cut
- status: animated
- type: pain_point
- persuasion: Pain agitation, stated as scope
- beat: accumulation
- blueprint: grid-card-assemble (Adapt)
- focal: none (typographic; filenames sourced from the terminal's own DATA tab)
- roles: none

Adapt: keep the staggered-cascade signature, but the array is two-tier — a settled chip cluster on
top and a cascade beneath it that deliberately **outruns the reader**. The overflow is the argument.

Scene 1 (0.0–1.6s): ground only, mono kicker `WHAT THAT NORMALLY COSTS` at top-left, numeral `02`
top-right. Nothing else. The emptiness reads against frame 01's resolved stack.

Scene 2 (1.6–4.2s): the four real filenames land as mono chips in a 2×2 cluster on the upper third,
staggered, each on a hard precise settle — `halcyon_income_statement.csv`,
`halcyon_balance_sheet.csv`, `halcyon_cash_flow.csv`, and last
`halcyon_billing_ledger.csv · 56.7K lines` in `fire-orange`, because it is the one carrying a row
count. Asymmetric cluster, ~45% of canvas.

Scene 3 (4.2–7.8s): a hairline wipes across under the cluster, then the work those files imply
cascades beneath it as a `/`-separated fadelist — `retype / re-link / tie out / bridge the variance /
rebuild the scenarios / re-run the covenants / re-cut the deck` — each item arriving on its own beat
with the stagger **accelerating**, opacity stepping down the stack (1.0 → 0.16). By the last two
items the cascade is faster than the line can be read. That is the point: the list does not resolve,
it outruns you.

Scene 4 (7.8–10.0s): the cascade halts mid-stack and `…AND AGAIN NEXT MONTH` types on in mono at the
bottom chrome line. The four chips hold their exact position, lit, while everything beneath them sits
at low opacity — staging the handoff.

- handoff_out: the four mono filename chips sit at y≈38% in a 2×2 cluster, scale 1.0, opacity 1 — Frame 3 catches them mid-fall.

## Frame 3 — Drop them in
- src: compositions/frames/03-drop-them-in.html

- scene: The filename chips fall into the terminal's real IS / BS / CF slots, which light amber and confirm
- duration: 9s
- transition_in: cut
- status: animated
- type: product_intro
- persuasion: The turn — the promise made concrete
- beat: resolution
- blueprint: cursor-ui-demo (Adapt)
- focal: assets/screen-load.png
- roles: screen-load = cutout (the hero surface, seated full-bleed behind the falling chips)
- asset_candidates: assets/screen-load.png

Adapt: keep the signature "the surface changes state shot-to-shot", but **there is no cursor** — the
chips carried over from frame 02 are what drive the state change. A cursor would read as a generic
SaaS demo; files falling into their own slots reads as the product's actual behaviour.

Scene 1 (0.0–1.4s): the four chips are already on screen at their frame-02 position, now falling.
Behind them the real DATA screen seats up from 96% scale and settles full-bleed — the product's first
appearance. Layered depth: screen background, chips foreground.

Scene 2 (1.4–4.4s): each chip reaches its slot and is absorbed — as it lands, that slot's dashed
border snaps to a solid `fire-orange` stroke, left to right: IS, then BS, then CF, then the OPS
ledger slot last. Four discrete state changes, each on its own beat, no two simultaneous.

Scene 3 (4.4–7.2s): the terminal's own console line types on beneath the slots in mono, caret
blinking — `> Loaded: Halcyon Cloud Systems, FY2023–FY2025 plus 56.7K billing lines through Aug 2026`.
The `Sample data` chip in the screen's header is legible throughout.

Scene 4 (7.2–9.0s): all four slots lit, console resolved, held. A low-amplitude jitter on the caret
only. The screen is now seated where frame 04 will continue from.

- handoff_in: the four chips enter at y≈38%, 2×2 cluster, scale 1.0, opacity 1, falling downward at ~340 px/s.
- handoff_out: the full terminal screen is seated full-bleed at scale 1.0, opacity 1, centered; Frame 4 continues from that same seat.

## Frame 4 — It reads the business back to you
- src: compositions/frames/04-reads-it-back.html

- scene: The dashboard seats, eight KPI tiles count up, then the mix donuts and the revenue bars draw in
- duration: 9s
- transition_in: cut
- status: animated
- type: feature_showcase
- persuasion: Value demonstrated, not described
- beat: payoff
- blueprint: dataviz-countup (Adapt)
- focal: assets/screen-dashboard.png
- roles: screen-dashboard = cutout (hero surface) · screen-variance = supporting (one cut late in the shot)
- asset_candidates: assets/screen-dashboard.png, assets/screen-variance.png

Adapt: keep the "numbers are the hero, camera lands on one hero metric" signature, but the camera
does **not** push through — it holds, and the count-ups plus the pillar rail do the work. A push here
would fight frame 05's continuous move.

Scene 1 (0.0–1.2s): the dashboard replaces the DATA screen in the same seat (same scale, same center
— a surface swap, not a new shot). The amber pillar rail draws down the left gutter and fills through
`DATA` and `ANALYZE`. Mono kicker `2 · ANALYZE` top-left.

Scene 2 (1.2–4.2s): the eight KPI tiles count up to their real values on a staggered start, tabular
figures, each tile's top hairline lighting as its number lands — $29.4M revenue, $21.4M gross profit,
72.8% gross margin, 295.8K units, $99 average price, 1,892 transactions, 1,367 active customers,
+51.6% new customers. The deltas resolve last, in the product's own green and red.

Scene 3 (4.2–6.6s): the revenue-by-month bars draw up left to right with the gross-margin line
tracking over them, then a hard cut to the variance bridges — budget → actual decomposed into price,
volume and mix — which draw in the same direction so the cut carries the curve.

Scene 4 (6.6–9.0s): the statement `it reads the business back to you.` reveals per word at h2 scale
over the lower-left, the screen dimming slightly behind it. Held read to the end — no push, no drift.

- handoff_in: terminal screen seated full-bleed, scale 1.0, opacity 1, centered.
- handoff_out: screen holds full-bleed at scale 1.0, opacity 1; the amber pillar rail sits at x≈6%, fully drawn through ANALYZE.

## Frame 5 — Plan it, stress it, decide it
- src: compositions/frames/05-plan-stress-decide.html

- scene: The pillar rail steps PLAN → DECIDE while the three-statement forecast, the Monte Carlo distributions and the NPV verdict hand off to each other
- duration: 13s
- transition_in: cut
- status: animated
- type: feature_showcase
- persuasion: Evidence block — depth that earns the memo
- beat: escalation
- blueprint: spatial-pan-stations (Reproduce)
- focal: assets/screen-invest.png
- roles: screen-model = supporting (station 1) · screen-montecarlo = supporting (station 2) · screen-invest = cutout (station 3, the landing)
- asset_candidates: assets/screen-model.png, assets/screen-montecarlo.png, assets/screen-invest.png

The densest frame, deliberately. Three stations pre-placed on one tall canvas, traversed by a single
vertical camera, landing held on the verdict.

Scene 1 (0.0–2.2s): station one — the integrated three-statement forecast, FY2026E → FY2030E. The
camera holds while the forecast table's columns reveal left to right. Rail steps to `PLAN`. Mono
kicker `3 · PLAN`.

Scene 2 (2.2–5.0s): the scenario toggle snaps `Pessimistic → Base → Optimistic`, and on each snap the
whole table re-reads — figures recomputing in place, not fading. Three discrete snaps. On the last,
the `Export model (.xlsx)` button catches an amber highlight sweep and holds lit. This is the beat
that says the output leaves the browser.

Scene 3 (5.0–8.2s): one continuous camera pan **down** to station two — Monte Carlo at 5,000
iterations. The EBITDA and ending-cash distributions draw in from their centers outward, then the
P10 / P50 / P90 markers drop into place with their values. Rail steps to `DECIDE`, kicker to
`4 · DECIDE`.

Scene 4 (8.2–11.2s): the pan continues down to station three — the investment case. The three figures
resolve one after another in the product's own red: `NPV −$421K`, then `IRR 9.5%`, then the verdict
`Reject` landing last and largest. No frame accent here; the red is the screenshot's own.

Scene 5 (11.2–13.0s): held on the verdict, camera stopped. The mono line
`IT COMPUTES THE ANSWER · IT DOES NOT FLATTER IT` types on the bottom chrome. The stillness after
eleven seconds of continuous travel is what makes the verdict land.

- handoff_in: amber pillar rail at x≈6%, opacity 1, drawn through ANALYZE.
- handoff_out: rail at x≈6%, opacity 1, drawn through DECIDE; the last screen holds at scale 1.0, opacity 1.

## Frame 6 — The memo writes itself
- src: compositions/frames/06-memo-writes-itself.html

- scene: The CFO memo's findings cascade in as severity rows, each red flag landing with its real number
- duration: 12s
- transition_in: cut
- status: animated
- type: benefit_highlight
- persuasion: The deliverable — the most expensive thing the terminal replaces
- beat: climax
- blueprint: agent-progress-theater (Adapt)
- focal: assets/screen-memo.png
- roles: screen-memo = cutout (hero surface)
- asset_candidates: assets/screen-memo.png

Adapt: keep the "receipt cascade whose rows arrive and resolve" signature. Drop the loader/spinner
theater entirely — the terminal is not an agent pretending to think, and a spinner would undercut
the credibility this frame exists to build. The rows simply arrive, already computed.

Scene 1 (0.0–1.8s): the memo surface seats. The title `sr fp&a memo to the cfo.` reveals per word at
h2 scale, left-anchored. The rail completes to `COMMUNICATE`, kicker `5 · COMMUNICATE`. The findings
area below is empty.

Scene 2 (1.8–4.0s): the first finding slides in from the left on a hard settle — `RED FLAG · DSO rose
8 days to 58 — about $6.8M of cash tied up`. The severity pill carries its own red; the figure
**$6.8M** lands in `fire-orange`. It holds long enough to read in full before anything else moves.

Scene 3 (4.0–6.0s): second finding — `RED FLAG · Mix shift to Professional services cut gross margin
2.7 pts`, amber on **2.7 pts**. The first row steps back to 70% opacity as it arrives, so the newest
finding always reads hardest.

Scene 4 (6.0–8.6s): third finding, the heaviest — `RED FLAG · Monte Carlo: 34.6% chance of a covenant
breach`, amber on **34.6%**. This one gets the longest hold of the four; it is the line that would
change a CFO's week, and it traces straight back to the distributions in frame 05.

Scene 5 (8.6–10.4s): fourth finding, deliberately quieter — `WATCH · EMEA $7.2M below budget —
volume, not price`, entering at reduced weight. The step down from RED FLAG to WATCH shows the
terminal grading severity rather than alarming indiscriminately.

Scene 6 (10.4–12.0s): the closing mono line `A BOARD-READY READ · DRIVERS · CASH · RISKS` types along
the bottom chrome, all four findings holding. Over the final 0.4s the whole surface scales to 1.04
and fades out as the ground returns to flat canvas.

- handoff_in: terminal screen full-bleed, scale 1.0, opacity 1.
- handoff_out: the memo screen scales 1.0 → 1.04 and fades to opacity 0 over the last 0.4s as the ground goes to flat canvas.

## Frame 7 — One terminal for the whole loop
- src: compositions/frames/07-one-terminal.html

- scene: The five pillars snap into a row, the hero line resolves, the wordmark locks up
- duration: 9s
- transition_in: cut
- status: animated
- type: branding
- persuasion: Identity, earned by the six frames behind it
- beat: sign-off
- blueprint: titlecard-reveal (Adapt)
- focal: none (typographic lockup; the hero line is the site's own)
- roles: landing-hero = background (not shown directly — its line and emphasis are reproduced in frame type)
- asset_candidates: assets/landing-hero.png

Adapt: keep the "one restrained move, then a still hold" signature, but run it as a short chain —
hero line, then pillars, then lockup — because the pillar row is the thing the previous six frames
earned and it deserves its own beat.

Scene 1 (0.0–1.4s): flat `ink-black` canvas, nothing carried over. The amber rule stub wipes
left-to-right on the upper third. Numeral `07` top-right. Maximum silence — this is the breath after
frame 06.

Scene 2 (1.4–3.8s): the hero line reveals per word at h1 scale, lowercase, left-anchored —
`from raw statements to a defensible valuation.` — with `defensible` landing in `fire-orange`, the
same emphasis the site itself uses on that exact word.

Scene 3 (3.8–5.8s): the five pillars snap into a single mono row beneath it on one shared beat —
`DATA · ANALYZE · PLAN · DECIDE · COMMUNICATE` — each already proven by a frame behind it. Hard
settle, no stagger: they arrive as a system, not a list.

Scene 4 (5.8–7.0s): a hairline wipes across the lower third and the lockup resolves beneath it —
`FP&A Terminal` at stat scale, `BUILT BY MINH-DUC THÉO HO` in mono, and on the right
`READS PITCHBOOK · 10-K PDF · CSV · EXCEL` above `EXPORTS LIVE-FORMULA EXCEL` in `fire-orange`.

Scene 5 (7.0–9.0s): **completely still.** No jitter, no drift, no residual motion anywhere in the
frame. Two full seconds of stillness close the film.

- handoff_in: flat canvas ground, no carry-over from Frame 6.
