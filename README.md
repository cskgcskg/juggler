# Siteswap Explorer 🤹
> An interactive, physics-based siteswap juggling pattern simulator built for the web.

## Overview
Siteswap Explorer is a web-based juggling simulator that goes beyond simple animations. It uses real parabolic physics, precise airtime calculations, and dynamic audio synthesis to create a realistic and educational visualization of juggling patterns. 

Whether you're exploring classic solo siteswaps like `531` or diving into complex 4-handed passing patterns like `786` (3-count), this tool breaks down the math and physics behind juggling in real time.

## ✨ Features

- **Physics-Based Engine**: Balls and clubs follow real-world parabolic arcs governed by gravity. Throw height correlates accurately with airtime.
- **Solo & Passing Modes**:
  - **Solo**: Explore standard siteswaps (e.g., cascades, fountains, showers, and complex mixed patterns).
  - **Passing**: Simulate two jugglers facing each other using 4-handed siteswap notation. Odd throws pass between jugglers, while even throws are self-throws.
- **Prop Customization**: Swap between balls and clubs. Adjust the number of spins for club throws (1×, 2×, 3×).
- **Live Trajectory Charts**: View real-time kinematics. Each prop gets its own mini-chart detailing the mathematical equation of its current parabolic flight ($y = v_0t - \frac{1}{2}gt^2$).
- **Generative Audio**: Employs the Web Audio API to procedurally generate distinct sound effects for throws, passes, and catches.
- **Adjustable Timing**: Dynamically tweak the tempo (BPM) and dwell ratio (the fraction of a beat the prop spends in the hand).
- **Preset Library**: Includes dozens of built-in patterns ranging from basic 3-ball cascades to intricate 7-object passing sequences.

## 🚀 Getting Started

The simulator is built entirely with vanilla web technologies (HTML, CSS, and JavaScript). No build steps or heavy frameworks are required.

To run the project locally:
1. Clone the repository.
2. Open `index.html` in any modern web browser.

## 🧠 What is Siteswap?

Siteswap is a mathematical notation used by jugglers to describe juggling patterns. Each digit represents how many "beats" a prop stays in the air:
- `3`: A standard throw that crosses to the other hand (e.g., 3-ball cascade).
- `4`: A higher throw that stays in the same hand (e.g., 4-ball fountain).
- `0`: An empty hand (a rest beat).
- `1`: A quick zip or handoff to the other hand.
- `2`: A momentary hold in the same hand.
- **Odd digits** change hands; **Even digits** return to the same hand.

### Passing Mode (4-Handed Siteswap)
In passing mode, beats alternate between Juggler A and Juggler B. 
- **Odd throws** cross between jugglers (passes).
- **Even throws** stay with the same juggler (selfs).
- *Example:* `7` is a classic 6-object pass (every throw crosses).

## 🛠️ Tech Stack
- **HTML5 Canvas:** Fully custom physics rendering and particle systems.
- **Vanilla JavaScript:** Zero dependencies. Custom scheduling, physics, and siteswap parsing engine.
- **Web Audio API:** Real-time synthesized sound effects (oscillators and gain ramps).
- **CSS3:** Modern UI with glassmorphism, responsive grid layouts, and animated gradients.

## ⚖️ License
[MIT License](LICENSE)
