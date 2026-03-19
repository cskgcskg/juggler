# 🤹 Siteswap Explorer

**A physics-based juggling pattern simulator** — enter any valid siteswap and watch it come to life with realistic parabolic arcs, sound effects, and a charming jester-hat-wearing juggler.

![Built with](https://img.shields.io/badge/Built%20with-HTML%20%2F%20CSS%20%2F%20JS-blueviolet)
![No dependencies](https://img.shields.io/badge/Dependencies-None-green)
![License](https://img.shields.io/badge/License-MIT-blue)

---

## ✨ Features

- **Real siteswap physics** — parabolic gravity arcs where taller throws take longer, just like real juggling
- **Balls & Clubs** — toggle between spherical balls and rotating clubs (single/double/triple spins based on throw height)
- **Pause & Resume** — freeze the simulation mid-air and resume seamlessly
- **Real-time controls** — adjust tempo (BPM) and dwell ratio live without restarting
- **Sound effects** — synthesised throw/catch sounds via Web Audio API (toggleable)
- **20+ preset patterns** — from basic cascade (`3`) to complex patterns like `b97531`
- **Detailed juggler** — animated character with jester hat, facial features, and glowing hands
- **Particle effects** — burst particles on throws and catches
- **Fully responsive** — works on desktop, tablet, and mobile
- **Zero dependencies** — single `index.html` file, no build step needed

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/cskgcskg/juggler.git

# Open in browser — that's it!
open index.html
```

Or simply download `index.html` and double-click to open.

## 🎮 How to Use

1. **Enter a siteswap** in the input field (e.g. `3`, `531`, `97531`)
2. **Click ▶ Juggle** to start the simulation
3. **Click ⏸ Pause** to freeze, **▶ Resume** to continue
4. **Switch props** between 🎾 Balls and 🪇 Clubs
5. **Adjust tempo** and **dwell ratio** in real-time while juggling
6. **Click any preset** to quickly load popular patterns

## 📖 Siteswap Notation

| Digit | Meaning |
|-------|---------|
| `0` | Empty beat (no ball) |
| `1` | Quick handoff |
| `2` | Hold (ball stays in same hand) |
| `3` | Standard 3-ball cascade throw |
| `4` | Fountain throw (returns to same hand) |
| `5+` | Higher throws with longer airtime |
| `a-z` | Values 10-35 (hex-style) |

**Odd** numbers cross to the other hand. **Even** numbers return to the same hand.

### Popular Patterns

| Pattern | Name | Balls |
|---------|------|-------|
| `3` | Cascade | 3 |
| `4` | Fountain | 4 |
| `531` | 531 | 3 |
| `441` | 441 | 3 |
| `51` | 3-Ball Shower | 3 |
| `97531` | 97531 | 5 |
| `b97531` | b97531 | 6 |

## 🛠 Tech Stack

- **HTML5 Canvas** — all rendering
- **Web Audio API** — synthesised sound effects
- **Vanilla CSS** — glassmorphism UI with responsive design
- **Vanilla JavaScript** — no frameworks, no dependencies
- **Google Fonts** — Inter + JetBrains Mono

## 🏗 Architecture

Everything lives in a single `index.html` file:

- **Siteswap validator** — validates patterns using the averaging rule
- **Physics engine** — calculates parabolic trajectories with real gravity
- **Beat scheduler** — maps ball positions to timing using BPM and dwell ratio
- **Renderer** — Canvas 2D drawing with trails, particles, and glow effects
- **Audio engine** — Web Audio oscillators for throw/catch feedback

## 📱 Browser Support

Works in all modern browsers:
- Chrome / Edge 80+
- Firefox 75+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Android)

## 📄 License

MIT — do whatever you want with it.
