# Siteswap Explorer 3D

An interactive, physics-based 3D juggling simulator powered by Three.js. Visualize siteswap patterns with realistic parabolic arcs, up to 4 jugglers, and 177 built-in presets.

## Overview

Siteswap Explorer started as a 2D canvas juggling simulator and evolved into a full 3D experience with detailed character models, real-time physics, procedural audio, and support for solo, passing, trio, and quartet juggling modes.

Whether you're exploring a simple 3-ball cascade (`3`) or pushing limits with a 13-object quartet feast (`d`), the simulator accurately computes parabolic trajectories, hand timing, and inter-juggler passes using siteswap mathematics.

## Features

**Physics & Rendering** -- Real parabolic arcs governed by gravity, rendered in 3D via Three.js r128 with PBR materials, 4K shadow maps, ambient floating particles, and dynamic lighting including key, fill, rim, hemisphere, and stage spot lights. ACES filmic tone mapping provides cinematic color.

**Four Juggling Modes** -- Solo (1 juggler), Passing (2 jugglers facing each other), Trio (3 jugglers cycling beats via `beat % 3`), and Quartet (4 jugglers cycling via `beat % 4`). Each mode has its own curated preset library.

**Three Prop Types** -- Balls (glossy spheres with specular highlights), Clubs (detailed multi-part geometry with handle, body, cap, and stripes), and Rings (torus geometry with inner highlight and edge glow). All props cast shadows and emit colored glow lights.

**Spin Control** -- Clubs and rings support configurable rotation: 0x Flat (helicopter/pancake), 1x, 2x, 3x, and 4x Pancake. Balls have no rotation. The spin selector adapts its options to the selected prop type.

**177 Built-in Presets** -- 73 solo patterns (cascades, fountains, showers, mills mess variations), 42 passing patterns (2-count through 7-count, chocolate bar, Jim's 3-count, and more), 26 trio patterns, and 36 quartet patterns ranging from 4-object beginner to 13-object expert.

**3D Character Models** -- Hand-crafted juggler models with expressive faces (eyes with irises, pupils, shine dots, eyelashes, blush), detailed hair (girl ponytail with scrunchie and bow, boy jester hat with bells), ears with earrings, articulated hands (palm, 4 fingers, thumb, wrist), and clothing details (girl dress with 'H' letter decal, waist ribbon, ruffle hem, red shoes; boy green t-shirt with 'S' letter, belt with buckle, sleeve cuffs, jeans, sneakers).

**Inverse Kinematics** -- Two-bone IK with pole vectors for natural arm movement. Elbows bend outward and slightly forward. Hand positions are smoothed via lerp interpolation to prevent jitter.

**Live Trajectory Chart** -- Real-time sidebar showing each prop's parabolic equation, peak height, airtime, and current position on the flight curve.

**Generative Audio** -- Web Audio API synthesizes distinct sounds for throws, catches, and passes using oscillator/gain ramp combinations. Toggle sound on/off anytime.

**Camera Controls** -- Click-drag to orbit around the scene. Scroll to zoom in/out. The camera automatically adjusts distance for each mode (closer for solo, wider for quartet).

## Getting Started

The entire application is a single HTML file with no build steps or dependencies (Three.js is loaded from CDN).

1. Clone the repository
2. Open `index.html` in any modern browser
3. It auto-starts in Passing mode with clubs -- click any preset to try different patterns

## What is Siteswap?

Siteswap is a mathematical notation for juggling patterns where each digit represents how many beats a prop stays in the air before landing. The number of objects equals the average of all digits.

A `3` is a standard crossing throw (3-ball cascade). A `5` goes higher and crosses. A `4` is a same-hand throw. A `0` is an empty beat. A `1` is a quick zip. Values above 9 use letters: `a`=10, `b`=11, `c`=12, etc.

In passing/trio/quartet modes, beats alternate between jugglers. A throw whose value lands on a different juggler's beat becomes a pass; otherwise it's a self throw.

## Tech Stack

- **Three.js r128** -- WebGL rendering with PBR materials, shadow mapping, and tone mapping
- **Vanilla JavaScript** -- Zero framework dependencies; custom siteswap parser, physics engine, IK solver, and simulator
- **Web Audio API** -- Procedural sound synthesis
- **CSS3** -- Glassmorphism panels, responsive layout, animated gradients

## Credits

Original 2D siteswap engine and UI by [The Best](mailto:cskgcskg@gmail.com).

3D conversion, Three.js rendering, character models, trio/quartet modes, ring props, spin system, graphics improvements, and expanded preset libraries built with [Claude Code](https://claude.ai/claude-code) by Anthropic (Claude Opus 4.6).

## License

[MIT License](LICENSE)
