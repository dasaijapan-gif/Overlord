# Overlord (working title)

A procedural world game for the browser. You are the overlord of a world that starts from nothing: a handful of
people in caveman times, on a seeded, generated island. You set the direction, make the economic decisions, pick
sides, intervene in crises and watch what your choices do to people as the settlement grows all the way to a city.

The world is a tilt-shift, low-poly diorama: a miniature seen from above, flat-shaded and saturated, with tiny
figures drawn with the least possible detail. The figures are simple, but the game tells stories through them anyway:
names, families, relationships, a living chronicle of what happens to them.

Both halves of human experience are real systems with real stakes. The dark side: gangs, political warfare,
economic collapse, fights, wars, famine, plague. The light side: harvests, festivals, births, weddings, inventions,
golden ages. The game is about the ebb and flow between them, and about the overlord's hand in it.

## Status

Day one. The design is being written and the first playable slice is being built. Everything in `docs/` describes
what the game is and how it is put together; `game/` holds the playable build.

## How it is built

- Plain HTML and ES modules, Three.js vendored from npm, no bundler, no asset pipeline: every mesh, figure,
  building and tree is generated in code.
- A deterministic, seeded simulation that runs headless in Node for tests and tuning, and a render layer that
  turns the simulation state into the diorama.
- Runs on a laptop and a phone, with mouse and touch.

## Run it

```
cd game
python3 -m http.server 8000
# open http://localhost:8000/
```
