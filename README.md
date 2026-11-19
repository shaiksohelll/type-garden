# Type Garden

An interactive generative typography canvas where words take root and bloom as you type. Built with zero dependencies using pure HTML5 Canvas and vanilla JavaScript.

**Live Demo:** [shaiksohelll.github.io/type-garden](https://shaiksohelll.github.io/type-garden/)

---

## Overview

**Type Garden** turns every keystroke into a living botanical composition. As characters appear in *Playfair Display*, procedural vines, thorns, leaves, and spiral roses sprout organically around and through the letterforms.

Each word generates its own seeded botanical traits—determining vine curvature, foliage density, rose frequency, and arched stem bridges between neighboring letters. The entire garden breathes with subtle hand-drawn line boil and leans softly toward your cursor as if caught in a gentle breeze.

## Features

* **Procedural Botanical Engine:** Generates multi-layered stems, thorns, veined leaves, curled tendrils, and blooming spiral roses that weave dynamically both behind and over the typography.
* **Word-Level Growth & Pruning:** Adjacent letters in a word connect via bezier stem bridges. Pressing **Space** prunes the completed word and blooms extra blossoms at its tips.
* **Tactile Motion & Physics:** Letters spring into place with damped oscillation, sway toward pointer movement, and animate with subtle frame-by-frame line boil.
* **10 Curated Color Palettes:** Switch instantly between high-contrast themes—including *Rose noir*, *Paper*, *Midnight*, *Citrus*, *Orchid*, *Moss*, *Tomato*, *Butter*, *Blush*, and *Mono*.
* **One-Click PNG Export:** Capture your typographic garden without the UI bar or blinking caret using the **PNG** button or `Ctrl/Cmd + S`.
* **Responsive & Touch-Ready:** Automatically scales and wraps multi-word compositions to fit desktop and mobile viewports, complete with hidden input mirroring for mobile keyboards.

## Controls

| Action | Desktop | Touch / Mobile |
| :--- | :--- | :--- |
| **Grow letters & flora** | Type any character | Tap canvas & type |
| **Prune word & bloom tips** | `Space` | `Space` |
| **Wither last character** | `Backspace` | `⌫` |
| **Clear canvas** | `Enter` | `Return` |
| **Export artwork** | Click `PNG` or `Ctrl/Cmd + S` | Tap `PNG` |

## Project Structure

```text
type-garden/
├── index.html      # Complete self-contained application (HTML, CSS, Canvas engine)
└── README.md       # Project documentation
