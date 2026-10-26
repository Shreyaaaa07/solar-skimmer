# ☀️ Solar Skimmer

**Solar Skimmer** is a fast, browser-based endless runner set against a pixel-art desert sunrise. Pilot Nova's solar-powered skimmer through the dunes, boost over rocks and pylons, duck beneath aerial drones, and see how far you can fly before the horizon catches you.

![License](https://img.shields.io/badge/license-MIT-blue.svg) ![Built%20with](https://img.shields.io/badge/built%20with-HTML%2C%20CSS%20%26%20JavaScript-f7a84d)

## Play

No build step, package manager, or server is required.

1. Clone or download this repository.
2. Open `index.html` in a modern web browser.
3. Press **Launch flight**, then use the controls below.

> For local development, you can also serve the folder with any static-file server, such as `python -m http.server`, and visit the displayed local URL.

## Controls

| Input | Action |
| --- | --- |
| `Space`, `↑`, or `W` | Boost / jump; starts or restarts a flight |
| Hold `↓` or `S` | Duck on the ground / dive while airborne |
| Click or tap the game canvas | Boost; starts or restarts a flight |
| Android touch controls | Tap **BOOST** to jump; hold **DUCK** to duck or dive |
| **Launch flight** button | Start a new flight |

## Gameplay

- The flight starts at a steady pace and accelerates continuously, up to a maximum speed.
- Avoid desert rocks and tall pylons by boosting over them.
- After reaching greater distances, moving drones join the hazard pool; duck or time your flight to avoid them.
- Your **Altitude** is displayed as the current distance score.
- **Best Flight** is saved in browser `localStorage`, so it remains available after refreshing or reopening the page in the same browser.
- After a collision, your final distance is shown and you can immediately launch another attempt.

## Features

- Standalone HTML5 Canvas game with no frameworks or external runtime dependencies
- Hand-drawn, low-resolution pixel-art scene rendered entirely in JavaScript
- Animated desert background, stars, sunrise, scrolling terrain, dust, and impact sparks
- Increasing difficulty through progressive speed and varied obstacles
- Keyboard, mouse, and Android touch controls, including a hold-to-duck button
- Responsive game shell with Android safe-area padding and touch-action handling
- Local persistent high score

## Project Structure

```text
solar-skimmer/
├── index.html   # Game layout, HUD, overlay, and accessible labels
├── style.css    # Responsive visual design and UI styling
├── game.js      # Canvas renderer, game loop, physics, input, scoring, and collisions
└── README.md
```

## How It Works

`game.js` runs a `requestAnimationFrame` loop that updates the game state and redraws the canvas every frame. The game uses simple gravity-based jump physics and axis-aligned bounding-box collision detection. Obstacles are generated one at a time with randomized dimensions and timing, while score and difficulty are derived from the distance travelled. Rendering is done with Canvas 2D primitives, preserving a crisp pixel-art look via disabled image smoothing.

## Browser Support

Solar Skimmer supports current evergreen browsers with HTML5 Canvas, `requestAnimationFrame`, ES6 JavaScript, and `localStorage`—including Chrome, Edge, Firefox, Safari, and current Android Chrome, Firefox, and Samsung Internet. On touch devices, on-screen **BOOST** and **DUCK** controls appear automatically.

## Development

The source is deliberately compact and dependency-free:

- Adjust game balance, obstacle generation, physics, or rendering in [`game.js`](./game.js).
- Update layout, colors, and responsive behavior in [`style.css`](./style.css).
- Change copy, semantic markup, and interface elements in [`index.html`](./index.html).

Because assets are drawn programmatically, there are no image or audio files to manage.

## License

No license file is currently included. Add a license before distributing or accepting contributions so usage rights are clear.
