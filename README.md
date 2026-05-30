# ✈ FROG CLASS 2.0 — A First-Class Crossing

A **first-person 3D reimagining of Frogger** with a luxury private-jet travel theme,
built for [Aspen Travel Advisors](https://github.com/aspentraveladvisors). You are a
frog of impeccable taste, late for a private jet — cross the arrivals boulevard and
the marina canal to reach your gate.

## What makes 2.0 a showpiece

- **Modern rendering** — HDR ACES tone mapping, real-time soft shadows, **bloom**, and
  a true **mirror-reflective canal** (`Reflector`) that mirrors the skyline + terminal.
- **Per-destination time-of-day** — every flight rebuilds the sky, fog, moon/sun and
  lighting: Aspen night, Santorini sunset, Maldives dawn, Dubai gold, Tokyo neon…
- **Procedural audio engine** — a generative lounge-music bed (pads, arpeggio, soft
  percussion) through convolution reverb, plus reactive SFX: hops, splashes,
  bell-like gate chimes, a fanfare, and a panned jet roar.
- **Living scene** — a departing private jet streaks overhead with afterburner +
  Doppler, sweeping searchlight beacons, animated palms, shimmering water, particle
  splashes and gate confetti.
- **Risk/reward scoring** — thread the traffic for **CLOSE CALL** bonuses and build a
  **streak multiplier**; cinematic fly-in intro on every flight.

All procedural — no image, audio, or model assets. One static `index.html`.

## Play

- **WASD / Arrow keys** (or the on-screen pad on touch) — hop one tile.
- **Drag** anywhere — look around in first person.
- **M** — mute.

Reach all **5 gates** to board your flight; each new flight is a new destination and a
gentle step up in difficulty (it starts deliberately calm). A radar shows nearby
traffic and craft. The boarding timer is generous — soak in the view.

> Degrades gracefully: if the post-processing / reflection add-ons are slow to load,
> the game falls back to a plain (still shadowed, tone-mapped) render and plays fine.

## Layout (faithful to the arcade original)

```
        ┌── 5 GATES (terminal / jet-bridges) ──────────────┐   ← goal
        │  yacht · Riva · vaporetto · water-taxi · gondola │   canal: ride the craft
        │  ——————— median lounge (safe) ———————            │
        │  G-Wagon · Tesla · stretch limo · Cybertruck ·   │   road: dodge the traffic
        │  Lamborghini                                     │
        └── red-carpet curb (start) ───────────────────────┘   ← you start here
```

## Tech

Single static `index.html` using [Three.js](https://threejs.org) r128 + a few
`examples/js` add-ons (EffectComposer/UnrealBloom/Reflector), all via CDN. No build
step. The original 2D arcade version is preserved at **`/classic`**.

## Deploy (Vercel)

Pure static site — no framework, no build. Import the repo into Vercel and it serves
`index.html` at the root automatically. `vercel.json` enables clean URLs so
`/classic` maps to `classic.html`.
