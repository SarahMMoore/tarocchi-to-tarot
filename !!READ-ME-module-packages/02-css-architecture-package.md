# CSS Architecture Package: Tarocchi to Tarot

---

## 1. CSS Organization & Directory Map

The production style package utilizes an explicit multi-file breakdown matching your exact workspace layout. This isolates components, avoids global naming collision, and keeps pages clean of bloated, unused rules.

```text
style/
├── global.css      # Custom Properties (Tokens), Cascade Layers, CSS Reset, Base Elements
├── layout.css      # Macro structural page bounds, header/footer wrappers, and viewports
├── index.css       # Home page profile boxes, gallery portals, and video sections
├── chapter.css     # Linear reading metrics and narrative content document wrappers
└── deck.css        # Archival card display matrices and missing asset placeholders
```

---

## 2. Cascade Strategy & Layer Order

To permanently isolate component dependencies and stop selector specificity wars, this design system implements native **CSS Cascade Layers (`@layer`)**. The precise processing hierarchy is locked in at the very first line of `style/global.css`:

```css
@layer reset, base, layout, component, utility, state;
```

### Source-Order Execution Order
1.  **`reset`**: Standardizes browser display baselines and enforces a solid `box-sizing: border-box` calculation.
2.  **`base`**: Manages default typography tags, fallback fonts, block element spacing, and body color fields.
3.  **`layout`**: Positions top-level page components (Header structures, main macro-grids, structural footer bands).
4.  **`component`**: Contains encapsulated, repeatable interfaces (Navigation arrays, portal panels, table rows).
5.  **`utility`**: Single-purpose helper classes equipped with `!important` to force specific style rules.
6.  **`state`**: Evaluates real-time layout changes tied to browser behavior cues (`:hover`, focus states, aria triggers).

---

## 3. Custom-Property (Design Token) System

Tokens are declared natively inside the root layer of `style/global.css` using your exact palette parameters to serve as the application's visual source of truth:

```css
@layer base {
  :root {
    /* --- Production Color Palette Tokens --- */
    --color-bg-center:    #ccc2b4;
    --color-bg-sidebar:   #6b211a;
    --color-bg-accent:    #143d30;
    --color-gold:         #ceaa64;
    --color-gold-bright:  #e5c17d;
    --color-text-light:   #dfd8cb;
    --color-text-dark:    #151514;

    /* --- Typographic Font Family Tokens --- */
    --font-body:          'Lora', 'Times New Roman', serif;
    --font-heading:       'IM Fell Great Primer', serif;
    --font-heading-sc:    'IM Fell English SC', serif;
    --font-heading-alt:   'IM Fell English', serif;

    /* --- System Rhythm Spacing Scale Tokens --- */
    --space-100: 0.5rem;
    --space-200: 1.0rem;
    --space-300: 1.5rem;
    --space-400: 2.5rem;
    --space-500: 5.0rem;

    /* --- Interactive Focus Indicator Rings --- */
    --focus-ring:         3px double var(--color-gold-bright);
    --focus-offset:       4px;

    /* --- Component-Scoped Tokens: Archival Deck Engine --- */
    --deck-grid-min:      280px;
    --deck-card-border:   1px solid var(--color-gold);
    --deck-card-shadow:   0 4px 12px rgba(0, 0, 0, 0.15);
  }
}
```

---

## 4. Component Patterns (Five Required Deployments)

These modular UI layouts are cleanly distributed across their corresponding architecture files.

### Pattern 1: Page Header Pattern (`style/global.css`)
```css
@layer component {
  .page-header {
    padding: var(--space-400) var(--space-200);
    text-align: center;
    background-color: var(--color-bg-accent);
    border-bottom: 2px solid var(--color-bg-accent);
  }

  .page-header h1 {
    font-family: var(--font-heading-sc);
    font-size: 2.5rem;
    margin-bottom: 0.5rem;
    color: var(--color-text-dark);
  }

  .page-header h2 {
    font-family: var(--font-heading-alt);
    font-style: italic;
    font-size: 1.5rem;
    color: var(--color-text-light);
    margin: 0;
  }

  .header-logo {
    max-width: 80px;
    height: auto;
    margin-bottom: var(--space-200);
  }
}
```

### Pattern 2: Global Responsive Site Navigation (`style/global.css`)
```css
@layer component {
  .site-nav {
    background-color: var(--color-bg-sidebar);
    border-bottom: 2px solid var(--color-gold);
  }

  .site-nav-list {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    flex-direction: column;
  }

  .site-nav-list a {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 44px; /* Strict WCAG 2.2 AA interactive target compliance */
    padding: var(--space-200);
    color: var(--color-text-light);
    font-family: var(--font-heading-alt);
    text-decoration: none;
    letter-spacing: 0.05em;
  }
  
  @media (min-width: 48rem) {
    .site-nav-list {
      flex-direction: row;
      justify-content: space-around;
    }
  }
}
```

### Pattern 3: Dashboard Gallery Portal Cards (`style/index.css`)
```css
@layer component {
  .gallery-section {
    padding: var(--space-400);
    background-color: var(--color-text-light);
    border-radius: 4px;
    border-top: 4px solid var(--color-bg-accent);
    box-shadow: 0 2px 8px rgba(21, 21, 20, 0.05);
  }

  .gallery-nav-list {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    flex-direction: column;
    gap: var(--space-200);
  }

  .gallery-nav-list a {
    display: block;
    padding: var(--space-200);
    background-color: var(--color-bg-accent);
    color: var(--color-text-light);
    font-family: var(--font-heading-alt);
    text-decoration: none;
    text-align: center;
    border-radius: 4px;
    border: 1px solid var(--color-bg-accent);
  }
}
```

### Pattern 4: Video Portal Block (`style/index.css`)
```css
@layer component {
  .video-section {
    padding: var(--space-400);
    background-color: var(--color-text-light);
    border-radius: 4px;
    border-top: 4px solid var(--color-bg-accent);
    box-shadow: 0 2px 8px rgba(21, 21, 20, 0.05);
  }

  .video-section h2 {
    font-family: var(--font-heading);
    font-size: 1.6rem;
    margin-bottom: var(--space-100);
  }
}
```

### Pattern 5: Site Footer Component (`style/global.css`)
```css
@layer component {
  .site-footer {
    padding: var(--space-500) var(--space-200);
    margin-top: var(--space-500);
    text-align: center;
    background-color: var(--color-bg-accent);
    border-top: 2px solid var(--color-gold);
  }

  .site-footer p {
    margin: 0.5rem 0;
    font-size: 0.95rem;
    color: var(--color-text-light);
  }

  .site-footer a {
    color: var(--color-gold);
    font-family: var(--font-heading-alt);
    text-decoration: none;
  }
}
```

---

## 5. Utilities and Dynamic States

### 5.1 Standalone Structural Utilities (`style/global.css`)
```css
@layer utility {
  .u-visually-hidden {
    position: absolute !important;
    width: 1px !important;
    height: 1px !important;
    padding: 0 !important;
    margin: -1px !important;
    overflow: hidden !important;
    clip: rect(0, 0, 0, 0) !important;
    white-space: nowrap !important;
    border: 0 !important;
  }

  .u-text-center {
    text-align: center !important;
  }

  .u-stack-flow > * + * {
    margin-top: var(--space-300) !important;
  }
}
```

### 5.2 Dynamic Interface States (`style/global.css`)
```css
@layer state {
  /* :hover Navigation Anchor Feedback States */
  .site-nav-list a:hover {
    background-color: rgba(255, 255, 255, 0.1);
    color: var(--color-gold-bright);
  }

  .site-footer a:hover {
    color: var(--color-gold-bright);
    text-decoration: underline;
  }

  /* :focus-visible Keyboard Focus Outline Rings */
  a:focus-visible,
  button:focus-visible {
    outline: var(--focus-ring) !important;
    outline-offset: var(--focus-offset) !important;
  }

  /* Active Location Indicator Context State */
  .site-nav-list a[aria-current="page"] {
    background-color: rgba(0, 0, 0, 0.2);
    border-bottom: 3px solid var(--color-gold-bright);
    color: var(--color-text-light) !important;
  }

  /* Accessible Elements Inactive State */
  [aria-disabled="true"] {
    opacity: 0.4;
    cursor: not-allowed;
    pointer-events: none;
  }
}
```

---

## 6. Print Support Layout Rules (`style/global.css`)

```css
@media print {
  /* Suppress elements not critical to academic paper prints */
  .site-nav, 
  .video-section, 
  .header-logo, 
  .site-footer a {
    display: none !important;
  }

  body {
    background: #ffffff !important;
    color: #000000 !important;
    font-size: 12pt;
    line-height: 1.5;
    font-family: 'Times New Roman', serif;
  }

  main, .main-index {
    display: block !important;
    width: 100% !important;
  }

  h1, h2, h3 {
    page-break-after: avoid;
    color: #000000 !important;
  }

  /* Append fully visible text URLs alongside anchors for print reference clarity */
  a::after {
    content: " (" attr(href) ")";
    font-size: 10pt;
    color: #444444;
  }
}
```

---

## 7. Refactoring Evidence (Before / After Records)

### Case 1: Cleaning Out Dead Layout-Section Code
*   **Before:** `style/index.css` contained a group selector `.gallery-section, .video-section, .layout-section` which applied shared border and container background fills to an old `layout-section` widget container template meant for card spreads.
* **after:** Completely removed .layout-section references from all style libraries and configuration sheets. This keeps the browser from spending processing power tracking and evaluating dead, unreferenced rules.

### Case 2: Replacing Isolated Spacing Calculations
* **Before:** Individual component style files relied on hardcoded pixel margins and padding settings (padding: 2.5rem 1rem; margin-top: 5rem;) declared manually across separate element wrappers.
* **After:** Linked structural elements directly to unified system tokens (var(--space-400), var(--space-500)). This update guarantees proportional layout rhythms across all browser contexts.

## 8. Architecture Notes
*  **Layer Strategy Decisions:** Organizing styles inside distinct @layer targets lets the system prioritize components based on layer order rather than selector complexity. This keeps class definitions short and simple.
*  **Token Decisions:** Properties draw cleanly from native variables. Layout sizes scale using standardized space ranges instead of pixel widths.
*  **Naming Approach:** Standard elements use clear lowercase hyphenated names (like .site-nav-list). Standalone visual overrides are prefixed with .u- to stay easily recognizable.
*  **Browser Checks:** Render layouts have been cross-checked to ensure that the flex containers handle text correctly without clipping columns on smaller viewports.
## 9. AI Disclosure Statement

### 9.1 Intended Use Cases
AI was used to organize structural component variables into CSS cascade layers, write clean fallback configurations for media print setups, and clear out dead style lines from older layout demonstrations.

### 9.2 Verification and Modifications
All generated components were checked directly against the active 4-file stylesheet repository. Shared portal class styles were updated to ensure only the .gallery-section and .video-section selectors are active on the home page dashboard.