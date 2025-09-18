# Hi, I'm Gurmeet 👋

<!-- Inline animated SVG header (rotating isometric cube) -->
<svg width="100%" height="220" viewBox="0 0 200 120" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Animated 3D cube">
  <defs>
    <linearGradient id="gTop" x1="0" x2="1">
      <stop offset="0" stop-color="#6EE7B7"/>
      <stop offset="1" stop-color="#3B82F6"/>
    </linearGradient>
    <linearGradient id="gLeft" x1="0" x2="1">
      <stop offset="0" stop-color="#60A5FA"/>
      <stop offset="1" stop-color="#7C3AED"/>
    </linearGradient>
    <linearGradient id="gRight" x1="0" x2="1">
      <stop offset="0" stop-color="#A78BFA"/>
      <stop offset="1" stop-color="#F472B6"/>
    </linearGradient>
    <filter id="softShadow" x="-50%" y="-50%" width="200%" height="200%">
      <feDropShadow dx="0" dy="6" stdDeviation="10" flood-opacity="0.18"/>
    </filter>
  </defs>

  <!-- group centered in the viewBox so rotation looks natural -->
  <g transform="translate(100,60)">
    <!-- continuous slow rotation around Z -->
    <animateTransform attributeName="transform"
                      type="rotate"
                      from="0 0 0"
                      to="360 0 0"
                      dur="8s"
                      repeatCount="indefinite" />

    <!-- isometric cube constructed from 3 polygons -->
    <!-- top face -->
    <g filter="url(#softShadow)">
      <polygon points="0,-36 36,-18 0,0 -36,-18"
               fill="url(#gTop)" stroke="#ffffff20" stroke-width="0.5"/>
      <!-- left face -->
      <polygon points="-36,-18 0,0 -36,36 -72,18"
               fill="url(#gLeft)" stroke="#00000010" stroke-width="0.5"/>
      <!-- right face -->
      <polygon points="36,-18 72,0 36,36 0,0"
               fill="url(#gRight)" stroke="#00000010" stroke-width="0.5"/>
    </g>

    <!-- subtle bobbing (Y translation) to add depth -->
    <animateTransform attributeName="transform"
                      type="translate"
                      values="0,0; 0,4; 0,0"
                      dur="2.8s"
                      additive="sum"
                      repeatCount="indefinite"/>
  </g>
</svg>

---

## About me
- 🚀 Full-Stack Developer & Competitive Programmer  
- 🔭 Currently working on cool projects (React, Node, LangChain etc.)  
- 💬 Ask me about optimization, algorithms, or building dev tools

---

## Quick links
- 🔗 My projects: `./projects`
- 📫 How to reach me: open an issue in this repo, or check my profile

---

## Customize this header
1. **Change colors** — edit the `<linearGradient>` stops in the SVG.
2. **Change rotation speed** — modify `dur="8s"` on the `animateTransform` that rotates the cube.
3. **Use as standalone image** — save the `<svg>...</svg>` block into `header.svg` and reference it with `![header](./header.svg)`.

---

## Higher-fidelity options
- **Interactive 3D (three.js / model-viewer):** GitHub READMEs do not allow arbitrary JS, so put an interactive demo on GitHub Pages (or CodePen) and link to it from your README.
- **True 3D animation GIF/WebP:** render a rotating 3D scene in three.js and export to GIF or WebP, then add it to README with `![3D header](./header.gif)`. (Better compatibility but larger file size.)

---

If you want, I can:
- generate a more complex SVG (animated particle tunnel, text morph, logo reveal), or
- give a quick three.js script and `ffmpeg` commands to produce a high-quality GIF/WebP you can embed.

Which would you like next?
