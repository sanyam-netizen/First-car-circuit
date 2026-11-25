# First Car Circuit

A 3D racing game built around the first car I ever modelled in Blender. I made the model, and the game code was written with Claude (Anthropic's AI assistant).

**Live demo:** [add your Vercel link here]

## About

I opened Blender for the first time and modelled a low-poly car in one day. Then I wondered what it would feel like to drive it, so I gave the model to Claude and had it build a game around it.

## Features

- Drive my own Blender model (the `.blend` file was converted into `car-data.json`)
- A 1.6 km circuit with three gates and a start/finish line
- Lap timer with best lap saved in the browser
- Handbrake drifting, nitro boost, tyre smoke and skid marks
- Three camera views: chase, top and cockpit
- Knockable cones, trees and a grandstand
- Engine and tyre sound effects
- Car paint colours, and a choice between a polished version and my exact model
- Works on laptops with the keyboard and on phones with on-screen buttons

## Controls

| Action | Keyboard | Phone |
|---|---|---|
| Drive | W A S D or arrow keys | Gas, Brake, left and right buttons |
| Handbrake drift | Space | Drift |
| Nitro | Shift | Nitro |
| Change camera | C | Camera |
| Back on track | R | Reset |
| Switch car version | V | Model |
| Mute | M | |
| Pause | P or Esc | Pause |

## Run it locally

The game loads the car with `fetch`, so open it through a local server instead of double-clicking the file:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## How it's built

- Plain HTML, CSS and JavaScript with a small custom WebGL renderer, with no game engine or libraries
- The car mesh is stored as base64 data in `car-data.json`
- Hosted as a static site on Vercel

## Credits

- Car model: made by me in Blender
- Game code: written by Claude, directed by me

## What's next

- Traffic cars
- A second track
- A ghost car that replays my best lap
