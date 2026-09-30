# Greatsword V3

A game launcher you can paste straight into Google Sites. It has 39 games from the Ultimate Game Stash, including Eaglercraft 1.12.2, and none of them use WebAssembly.

## Add it to Google Sites

1. Open `index.html` and copy all of it.
2. In Google Sites, go to **Insert → Embed → Embed code**, paste it, and click **Next → Insert**.
3. Drag the embed box to make it big. The **Fullscreen** and **New tab** buttons give you more room.

The embed code is small (~11 KB). Each game file is downloaded from the `games/` folder of this repo when you click it, so the repo has to stay **public** and the files need to be on the `main` branch (the launcher also checks the `claude/vigilant-turing-qncum6` branch as a fallback).

## Credits

Game files come from the Ultimate Game Stash (via the DogeSploit/UGS-Main rehost). All rights belong to their original creators.

## PolyTrack (no-WASM build)

PolyTrack normally needs WebAssembly for its physics engine and math. `games/polytrack.html` is a patched copy: the physics engine and math module were converted to plain JavaScript with Binaryen's `wasm2js`, and 3D models use three.js's pure-JS Draco decoder. It works in browsers where WebAssembly is disabled.
