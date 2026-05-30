# ✈ FROG CLASS — A First-Class Crossing

A **first-person 3D reimagining of Frogger** with a luxury-travel theme, built for
[Aspen Travel Advisors](https://github.com/aspentraveladvisors). You are a frog of
impeccable taste, late for a private jet — cross the arrivals boulevard and the
marina canal to reach your gate.

Retro arcade soul (chiptune SFX, CRT scanlines, chunky pixel rendering, flat-shaded
low-poly), seen entirely from the frog's own eyes. **Look around** and you'll find
your snout, eye-bulges and webbed hands in view — you really are the frog.

## Play

- **WASD / Arrow keys** (or the on-screen pad on touch) — hop one tile.
- **Drag** anywhere (or the look-pad on touch) — look around in first person.
- **M** — mute.

Reach all **5 gates** to board your flight; each new flight is a new destination
(Aspen, Monaco, Dubai, Maldives, St. Moritz…) and a gentle step up in difficulty.
A radar in the corner shows nearby traffic and craft. Mind the boarding timer.

## Layout (faithful to the arcade original)

```
        ┌── 5 GATES (terminal / jet-bridges) ──┐   ← goal
        │   yachts · luggage barges · canal    │   river: ride the craft
        │   ——— median lounge (safe) ———       │
        │   limos · car service · shuttles     │   road: dodge the traffic
        └── red-carpet curb (start) ───────────┘   ← you start here
```

## Tech

Single static `index.html` using [Three.js](https://threejs.org) (r128, via CDN).
No build step. The original 2D arcade version is preserved at **`/classic`**.

## Deploy (Vercel)

Pure static site — no framework, no build. Import the repo into Vercel and it serves
`index.html` at the root automatically. `vercel.json` enables clean URLs so
`/classic` maps to `classic.html`.
