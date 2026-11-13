# Paper Workshop / Бумажная мастерская

Interactive 3D paper-craft web application: paint ready-made 3D shapes or build multi-part paper toys from primitives, unfold them automatically onto A4 sheets with fold lines and glue tabs, and print them directly from your browser.

Zero build step — runs from a single [`index.html`](index.html) file using vanilla HTML/CSS/JS and Three.js (`r128`).

## Languages

- **Russian (default)** & **English**: use the **`RU | EN`** toggle in the header, open [`index.html?lang=en`](index.html?lang=en), or open [`en/index.html`](en/index.html).

## Features

- **Two modes**:
  - **Shapes (`Фигурка`)**: 16 ready-made 3D models (Cube, Pyramid, House, Crystal, Pine tree, Lantern, Icicle, Sphere, Tetrahedron, Tent, Cup, Barrel, Diamond, Rocket, Chest, Tower) with live A4 sheet scaling (`50%–100%`).
  - **Builder (`Конструктор`)**: assemble custom multi-part crafts from 6 centered primitives (Box, Cylinder, Sphere, Cone, Pyramid, Wedge), load the built-in bear preset, duplicate or mirror parts, rename parts, and pack nets automatically across one or more A4 pages for a chosen target height (`5–30 cm`).
- **Blender-style 3D gizmos (Builder mode)**:
  - **`G` — Move (`Двигать детали`)**: drag along the floor plane or X/Y/Z axis arrows.
  - **`R` — Rotate (`Поворот`)**: drag world X/Y/Z rings or outer screen-space ring (also supports `+15°` side-panel buttons).
  - **`S` — Scale (`Масштаб`)**: drag local X/Y/Z handles or the outer uniform ring (`0.2–3.0`) without losing face textures.
  - **`Delete` / `Backspace`**: remove the selected part.
- **3D & flat-net painting**:
  - Paint directly on the 3D surface or onto the A4 unfolded net (`Shapes` mode).
  - Kid-friendly UI with cheerful tools: Brush (`1–10`), Fill Bucket (`🪣`) with 10 procedural patterns (solid, dots, stripes, diagonal, checkerboard, grid, zigzag, waves, stars, hearts) replacing surfaces cleanly without layering, Stickers (`⭐`), and Eraser (`🧽`).
  - Single-side actions (`🎨 Fill side`, `🧽 Clear side`) alongside whole-model actions (`✨ Paint all`, `🗑️ Clear all`).
- **Undo / Redo history**:
  - Full Undo/Redo (`Ctrl+Z` / `Cmd+Z`, `Ctrl+Shift+Z` / `Cmd+Shift+Z` or `Ctrl+Y`) for painting strokes as well as moves, rotations, and scaling.
- **Print & save**:
  - Generates print-ready A4 sheets with solid cut lines, dashed fold lines, gray glue tabs, custom signature, and legend.
  - Auto-saves locally in `localStorage` and supports `.paper.json` export/import.

## Running Locally

Clone the repository and open [`index.html`](index.html) in a browser (internet access is needed only to load Three.js and the Rubik font from CDNs):

```bash
git clone https://github.com/Ivan3232j/paper-work.git
cd paper-work
open index.html
```

Or serve statically with any HTTP server:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000/` (Russian) or `http://localhost:8000/en/` (English).

## О проекте (RU)

**Бумажная мастерская** — однофайловое 3D веб-приложение для создания бумажных фигурок с дружелюбным для детей интерфейсом: можно раскрашивать готовые модели прямо в 3D или на развёртке, заливать отдельные стороны или всю фигурку цветом и узорами (10 процедурных паттернов без наложения слоёв: сплошная, горошек, полоски, диагональ, шахматка, клетка, зигзаг, волны, звёздочки, сердечки), стирать краску с конкретной стороны (`🧽 Стереть сторону`), собирать игрушки из деталей в режиме конструктора с инструментами перемещения (`G`), поворота (`R`) и масштаба (`S`) как в Blender, отменять и возвращать действия (`Ctrl+Z` / `Ctrl+Shift+Z`), сохранять проекты в `.paper.json` и печатать готовые листы А4 с линиями сгиба и клапанами для склейки.
