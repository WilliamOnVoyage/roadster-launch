# Roadster Launch

A browser stunt game built with three.js: launch up a reverse-C ramp, come off it upside down, roll upright and jet-land, then hop the line-up. Or switch to rocket mode and fly to Mars. Solo or online with other players, with a paint shop and a global leaderboard.

**Play:** https://roadsterarena.dev/ (free, no install, no login; keyboard or touch)

Made by [@nathangu76](https://x.com/nathangu76).

## Run it locally

The models load with `fetch()`, so serve the folder instead of opening the file directly:

```bash
python3 -m http.server 8000
```

then open http://localhost:8000/

## What's inside

- `index.html`: the whole game (physics, rendering, volumetric smoke, synthesised audio, UI). three.js 0.160 is loaded from jsDelivr.
- `models/`: meshopt-compressed glTF models (car, line-up vehicles, pilot).
- `voice.js`, `smoke.js`: the finale voice clip and a fallback smoke atlas.
- `ai.js`: recorded runs that AI drivers replay when an online room is quiet.

Online play (rooms, leaderboard, paint jobs) talks to a small Cloudflare Worker at `api.roadsterarena.dev`.

## License

The code and the original assets in this repository (the procedural scene, the synthesised music and sound, the original pilot character) are released under the [MIT License](LICENSE).

This is an unofficial fan-made project. It is not affiliated with, endorsed by, or sponsored by Tesla or any other car maker. "Tesla" and "Roadster" are trademarks of their respective owners, and the vehicle designs belong to them; the MIT License grants no rights to any trademark, logo or vehicle design.
