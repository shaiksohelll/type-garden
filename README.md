# Type Garden

> *A generative typography playground where words take root, sprout vines, and bloom as you type.*

[![Live Demo](https://img.shields.io/badge/Live_Demo-GitHub_Pages-FF1400?style=for-the-badge)](https://shaiksohelll.github.io/type-garden/)
[![Built With](https://img.shields.io/badge/Canvas_2D-Vanilla_JS-111111?style=for-the-badge)](#architecture--mechanics)
[![Dependencies](https://img.shields.io/badge/Dependencies-Zero-3257FF?style=for-the-badge)](#local-setup)

**Experience it live:** **[shaiksohelll.github.io/type-garden](https://shaiksohelll.github.io/type-garden/)**

---

## About the Project

**Type Garden** turns an ordinary blank screen into an interactive botanical print. Every letter you type is set in bold *Playfair Display* serif typography and immediately acts as soil for a real-time procedural flora engine[cite: 1]. 

Rather than using pre-made sprites or static SVGs, every stem, thorn, veined leaf, curled tendril, and spiral rose is drawn mathematically on an HTML5 `<canvas>` at 60fps—weaving dynamically both behind and over the letterforms as your sentence grows[cite: 1].

## Key Highlights

* **Word-Seeded Botanical DNA:** Every continuous word generates its own deterministic seed (`wordParams`) controlling stem curvature, foliage density, lean angle, and blossom frequency—so no two words grow alike[cite: 1].
* **Inter-Letter Stem Bridges:** Characters within the same word link together using cubic Bézier vine arches, turning individual letters into cohesive typographic bouquets[cite: 1].
* **Organic Physics & Line Boil:** Letterforms enter with damped spring oscillation, sway gently toward your cursor's gravitational reach, and shimmer with a subtle frame-by-frame hand-drawn boil[cite: 1].
* **10 High-Contrast Color Themes:** Switch palettes on the fly—from dark editorial contrasts (*Rose noir*, *Midnight*, *Orchid*, *Mono*) to warm print-inspired tones (*Paper*, *Tomato*, *Butter*, *Blush*, *Citrus*, *Moss*)[cite: 1].
* **Clean PNG Export:** Save a high-DPI snapshot of your current composition (with the UI bar and blinking caret automatically hidden) via the **PNG** button or `Ctrl/Cmd + S`[cite: 1].

## Keyboard & Touch Interactions

| Input | Behavior |
| :--- | :--- |
| **Letters / Characters** | Sprouts a new letterform and seeds upward, downward, and bridging vines[cite: 1] |
| **`Space`** | Prunes the active word, triggering extra terminal blossoms and tendrils[cite: 1] |
| **`Backspace` / `⌫`** | Withers the last character while letting its surrounding flora fade out gracefully[cite: 1] |
| **`Enter` / `Return`** | Clears the garden and resets the canvas[cite: 1] |
| **Cursor / Pointer** | Bends nearby stems and roses softly toward pointer coordinates[cite: 1] |
| **`Ctrl/Cmd + S` or `PNG`** | Renders a clean frame and downloads `garden.png`[cite: 1] |

## Architecture & Mechanics

The entire application lives inside a single, self-contained `index.html` file (~15 KB) with zero build tools or external JavaScript libraries:

* **Two-Pass Layer Weaving:** Each vine segment is assigned a front (`1`) or back (`0`) z-layer during generation, allowing stems and roses to weave organically behind and in front of the rendered text pass[cite: 1].
* **Dynamic Auto-Fitting Layout:** A binary-search text-wrapping solver (`layoutCore`) continuously recalculates font size and multi-line wrapping as you type or resize the viewport[cite: 1].
* **Mobile Input Mirroring:** Uses a zero-width sentinel character (`\u200B`) inside a hidden `<input>` to diff mobile virtual keyboard events and IME compositions accurately[cite: 1].

## Local Setup

```bash
git clone [https://github.com/shaiksohelll/type-garden.git](https://github.com/shaiksohelll/type-garden.git)
cd type-garden
