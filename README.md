# CSS Layout Lab

An interactive Flexbox & Grid explorer — **change properties, see the layout update instantly**. Built for learning CSS layout through hands-on experimentation.

## What is this?

CSS Layout Lab is a visual, code-first tool that teaches Flexbox and Grid by letting you:
- Toggle layout properties with dropdowns and sliders
- See the preview update in real-time
- Copy the generated CSS to use anywhere
- Get hints from Les, the talking `<` symbol

No theory, no clicking around in the dark. Change a value → see what happens.

## Features

### Phase 1: Flexbox (Live)
- **5 core properties:**
  - `flex-direction` (row, column, reverse variants)
  - `justify-content` (6 alignment options)
  - `align-items` (5 variants)
  - `gap` (slider, 0-40px)
  - `flex-wrap` (wrap handling)

- **Live preview** with 3 sample items
- **Real-time CSS output** — copy with one click
- **Les the mascot** — animated character with contextual tips
- **State persistence** — your settings auto-save to localStorage

### Phase 2: Grid (Coming soon)
- Interactive grid property builder
- Visual grid lines and cell highlighting
- Auto-placement visualization
- Template builder

## How to use

1. **Open** `css-layout-lab-flexbox.html` in your browser
2. **Adjust controls** on the right:
   - Select a value from any dropdown
   - Drag the gap slider
3. **Watch the preview** update instantly on the left
4. **Copy the CSS** with the "Copy CSS" button
5. **Paste it** into your own project

### Reading tips from Les
- Click **"Next tip"** to cycle through helpful explanations
- Click **"Mute"** to hide Les (preference saved)
- Les appears again if you clear localStorage

## Code structure

```
css-layout-lab-flexbox.html
├── Style (gradient header, dark theme, responsive grid)
├── HTML (controls, preview, code output, Les character)
└── JavaScript
    ├── state object (tracks all property values)
    ├── render() (updates preview + code)
    ├── Event listeners (on control changes)
    ├── localStorage persistence
    └── Les tip cycling
```

### Key concepts used
- **CSS Grid** for the lab layout (preview + controls side-by-side)
- **Flexbox** in the preview container (the thing being styled)
- **CSS animations** for Les (bounce, smile, wave, look-around)
- **Dynamic CSS application** via `style` properties
- **Template literals** for code generation

## Customization

### Change the sample items
Edit the HTML to add more or different items:
```html
<div class="preview-container" id="preview">
  <div class="preview-item">1</div>
  <div class="preview-item">2</div>
  <div class="preview-item">3</div>
  <!-- Add more -->
</div>
```

### Change the color scheme
Edit CSS variables at the top:
```css
:root {
  --bg: #0b1020;
  --card: #121a2a;
  --text: #eaf1ff;
  --muted: #7f8aa3;
  --blue: #4aa3ff;
  --green: #3ef0a8;
}
```

### Add more tips for Les
Expand the `tips` array in JavaScript:
```javascript
const tips = [
  "Existing tip...",
  "Your new tip here",
  // Add more
]
```

## Browser support
- Chrome/Edge: ✅ Full support (animations, localStorage)
- Firefox: ✅ Full support
- Safari: ✅ Full support
- IE11: ❌ Not supported (CSS Grid, animations)

## What's next?

### Phase 2: Grid properties
- `grid-template-columns` (visual builder)
- `grid-template-rows`
- `gap`
- `justify-items` / `align-items`
- `grid-auto-flow`
- Visual grid overlay

### Phase 3: Advanced
- Side-by-side Flexbox + Grid comparison
- Responsive breakpoint simulator
- Save/share layouts (via URL params or JSON)
- More Les expressions (sad, excited, thinking)

## Running locally

No build step needed. Just:
1. Save the `.html` file
2. Open in a browser
3. Start experimenting

If you want to edit:
- Use any text editor (VS Code, Sublime, etc.)
- Save the file
- Refresh the browser

## Want to extend it?

The code is heavily commented. Look for:
- `// State` — data structure
- `// Event listeners` — how controls wire up
- `// Main render` — how preview + code sync
- `// Les controls` — mascot logic

Good starting points for adding features:
1. Grid properties (copy the Flexbox control pattern)
2. More animation types (modify `@keyframes`)
3. Export layouts as JSON (extend `copyCode()`)

## Credits

**Design inspiration:** Microsoft Clippy (but actually helpful 😄)

**Built for:** Learning by doing, not reading docs.

---

Have a question? Stuck on a property? Check what Les has to say — he probably has a tip for it.
