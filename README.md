*This is a submission for [Weekend Challenge: Earth Day Edition](https://dev.to/challenges/weekend-2026-04-16)*

## What I Built

**Women in Tech — Global Map** 🌍💖

An interactive, pixelated 3D globe that visualizes the percentage of the tech workforce that is female in countries around the world. The project highlights the global gender gap in technology through a beautiful pink-themed, retro-pixel aesthetic.

### Features

- **3D Rotating Globe** — A low-poly, flat-shaded icosahedron globe that auto-rotates and can be dragged to explore
- **57 Country Data Points** — Pixelated box columns rise from each country, with height and color mapped to female tech participation rates
- **Interactive Tooltips** — Hover over any country marker to see its name, percentage, region, and a progress bar
- **Stats Panel** — Live stats including global average, country count, highest (Philippines 46%), and lowest (Pakistan 9%)
- **Pixelated Retro Style** — Low pixel ratio rendering, flat shading, scanline overlay, "Press Start 2P" pixel font, and crisp-edges rendering
- **Pink Aesthetic** — Entire color palette in shades of pink, magenta, and rose — from the deep dark background to glowing markers and star field

## Demo

Open `index.html` in any modern browser — no build step or server required!

## Code

A single `index.html` file using:
- **Three.js** (v0.170) for 3D rendering via ES module imports from CDN
- **OrbitControls** for drag-to-rotate and scroll-to-zoom interaction
- **Pure CSS** for the pixel UI, scanline overlay, and pink theme
- **Inline data** sourced from World Bank, UNESCO, Deloitte, and McKinsey reports (approximate figures)

## How I Built It

The globe is an `IcosahedronGeometry` with flat shading to get a low-poly, pixelated look. The renderer pixel ratio is intentionally set low (`1/3`) so the entire canvas renders at a fraction of screen resolution and is scaled up with `image-rendering: pixelated` — giving everything that chunky retro-pixel feel.

Each country is represented by a `BoxGeometry` column positioned on the globe surface using lat/lon → spherical coordinate conversion. Column height and color both encode the female tech workforce percentage, creating a gradient from deep magenta (low %) to bright pink (high %).

A raycaster handles mouse hover detection on the 3D markers, showing a pixel-bordered tooltip with country details. The scene includes a pink star field, latitude/longitude grid lines, a glow shell, and a CSS scanline overlay for extra retro vibes.

## Prize Categories

Best Use of GitHub Copilot

<!-- Team Submissions: Please pick one member to publish the submission and credit teammates by listing their DEV usernames directly in the body of the post. -->

<!-- Thanks for participating! -->
