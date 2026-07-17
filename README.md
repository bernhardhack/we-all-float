# WE ALL FLOAT

*A sewer-crawler arcade tragedy — in the tradition of knights who lose their armor.*

An endless side-scrolling action platformer in a single HTML file. No build step,
no dependencies, no external assets. Every sprite is canvas primitives; every
sound — including the darkwave soundtrack — is generated live with the Web Audio API.

A loving reply to [Paradise Souls](https://mihaicata.github.io/Paradise-Souls/):
he answered Milton, this answers the sewers of Derry.

## Play

Open `index.html` in any modern browser. That's it.

## Rules of the Barrens

- **The raincoat is the armor.** One hit shreds it. The second hit — you float.
- Endless sewer, endless enemies. Distance is the only score that matters.
- Every few hundred meters, **the clown comes up from the drain**. Hurt it enough
  and it stops pretending to be a clown. Beat it and it leaves behind a fresh
  raincoat — the only way to get your armor back.
- **Rocks** arc and take two hits to put a townsperson down.
  Pop a red balloon and it might drop the **silver slug** — flat, fast, and it
  actually works.
- Red balloons drift on sine waves and drop enemies on your head. Jump-throw to
  pop the high ones. **Duck** to hit the leeches.

## Controls

| Key | Action |
|---|---|
| ← → | run |
| ↑ | jump — press again mid-air to double jump |
| ↓ | duck (lowers your throw) |
| Space | throw |
| M | mute |
| Enter | start / go back down |

## Difficulty

Choose on the title screen with ↑/↓:

- **Losers' Club** — a fighting chance. Slower enemies, calmer spawns, a longer
  mercy window after losing the coat.
- **Derry Classic** — the arcade keeps your quarter. For people who think
  Ghosts 'n Goblins was reasonable.

## Deploy on GitHub Pages

1. Push this folder to a repo.
2. **Settings → Pages → Deploy from a branch** → `main`, root.
3. Live at `https://<you>.github.io/<repo>/` a minute later.

## Tech notes

Single file, vanilla JS, HTML5 Canvas. Fixed-timestep-ish rAF loop, gravity +
AABB collision, parallax brick/pipe layers drawn procedurally, particle system,
and a 100 BPM E-minor sequencer (sawtooth bass, kick, off-beat hats, cold pads)
scheduled with a Web Audio lookahead timer.

Tuning knobs live at the top of the script: the `DIFFS` table controls spawn
pacing, enemy speed, drop rates, and the post-hit mercy window.

## License

MIT — see `LICENSE`.
