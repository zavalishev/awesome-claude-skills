---
name: algorithmic-art
description: "Creating algorithmic art using p5.js with seeded randomness and interactive parameter exploration. Use for generative art, flow fields, particle systems."
source: https://github.com/anthropics/skills
---

# Algorithmic Art (p5.js)

Create algorithmic art through computational philosophy and code.

## Two-Step Process

1. **Algorithmic Philosophy Creation** (.md file)
2. **Express in p5.js** (.html + .js files)

## Step 1: Algorithmic Philosophy

Create a VISUAL PHILOSOPHY expressed through:
- Computational processes, emergent behavior, mathematical beauty
- Seeded randomness, noise fields, organic systems
- Particles, flows, fields, forces
- Parametric variation and controlled chaos

### How to Generate

**Name the movement** (1-2 words):
- "Organic Turbulence"
- "Quantum Harmonics"
- "Emergent Stillness"

**Articulate the philosophy** (4-6 paragraphs):
- Computational processes and mathematical relationships
- Noise functions and randomness patterns
- Particle behaviors and field dynamics
- Temporal evolution and system states

### Philosophy Examples

**"Organic Turbulence"**
Chaos constrained by natural law. Flow fields driven by layered Perlin noise. Thousands of particles following vector forces, their trails accumulating into organic density maps.

**"Quantum Harmonics"**
Discrete entities exhibiting wave-like interference patterns. Particles on a grid, each carrying a phase value that evolves through sine waves. Interference creates bright nodes and voids.

**"Field Dynamics"**
Invisible forces made visible through their effects on matter. Vector fields constructed from mathematical functions. Particles born at edges, flowing along field lines.

## Step 2: p5.js Implementation

### Technical Requirements

**Seeded Randomness:**
```javascript
let seed = 12345;
randomSeed(seed);
noiseSeed(seed);
```

**Parameter Structure:**
```javascript
let params = {
  seed: 12345,
  particleCount: 1000,
  noiseScale: 0.005,
  speed: 2,
  // Add parameters that control YOUR algorithm
};
```

**Canvas Setup:**
```javascript
function setup() {
  createCanvas(1200, 1200);
}

function draw() {
  // Your generative algorithm
}
```

### Express the Philosophy Through Code

**If philosophy is about organic emergence:**
- Elements that accumulate or grow over time
- Random processes constrained by natural rules
- Feedback loops and interactions

**If philosophy is about mathematical beauty:**
- Geometric relationships and ratios
- Trigonometric functions and harmonics
- Precise calculations creating unexpected patterns

**If philosophy is about controlled chaos:**
- Random variation within strict boundaries
- Bifurcation and phase transitions
- Order emerging from disorder

### Output Format

Single HTML artifact containing:
- p5.js from CDN
- All algorithm code inline
- Parameter controls (sliders, color pickers)
- Seed navigation (prev/next/random/jump)

### Required Features

1. **Parameter Controls** - Sliders for numeric params, real-time updates
2. **Seed Navigation** - Display seed, prev/next/random buttons, jump to seed
3. **Self-Contained** - No external files except p5.js CDN

## Craftsmanship Requirements

- **Balance**: Complexity without visual noise
- **Color Harmony**: Thoughtful palettes, not random RGB
- **Composition**: Visual hierarchy and flow
- **Performance**: Smooth execution
- **Reproducibility**: Same seed = identical output
