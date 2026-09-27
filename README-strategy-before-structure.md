# GIT 414 Project Specification & Documentation Map
## Project Title: Tarocchi to Tarot

---

## 🏛️ Part 1: GIT 414 Website Planning Specification Matrix

### 1. Purpose
* **Primary Objective**: The site helps people understand that tarot cards originated as a **secular, 15th-century Northern Italian court card game (Tarocchi)** rather than a tool for witchcraft or divination. It traces the deck's complete 600-year mechanical, cultural, and psychological evolution.
* **Core Takeaways**:
  * **Chapter 1**: Card play originated in Tang Dynasty China, traveled through Mamluk Egypt, and its trumps were structurally inspired by Francesco Petrarch’s poem *I Trionfi*.
  * **Chapter 2**: The original game featured a rigid 78-card architecture (56 suited cards, 22 trumps) that acted like a programming short-circuit loop to interrupt trick-taking gameplay flow.
  * **Chapter 3**: 18th-century French Enlightenment salons invented the Egyptian myth (*Book of Thoth*), introduced the first professional readings, and mapped cards to the Hebrew alphabet.
  * **Chapter 4**: 20th-century psychologists mapped the cards to Carl Jung's archetypes, using layouts like the Celtic Cross as a secular catalyst for cognitive projection.
  * **Chapter 5**: Modern software engineering and game design use Tarot as a multi-dimensional relational database schema and a core benchmark for training multimodal artificial intelligence systems.

### 2. Audience
* **Target Users**: Academic researchers, graphic design students, history buffs, game design developers, and contemporary secular tarot practitioners looking for a historically accurate, research-backed perspective on playing cards.
* **Conditions Affecting Use**: High-density scanning across variable environments. Because visitors parse highly complex rules, historical matrices, and multi-tier lists on a table while physically holding paper cards, the text must be formatted with pristine typographic contrast. It must scale dynamically from broad desktop layouts down to touch-friendly mobile views.

### 3. Content
* **Information & Copy**: Five comprehensive historical chapters mapping the global timeline from 9th-century China to 21st-century machine learning frameworks.
* **Media Assets**: High-resolution responsive image portfolios including Chinese money-suited variants, Mamluk designs, Pesellino's *Triumphs*, Visconti-Sforza gold leaf trumps, Tarocco Bolognese woodcuts, and French suit transformation graphics.
* **Tables**: *Table 1.1: Literary & Tarot Archetype Parallels* (Chaucer's pilgrims mapped to major archetypes) and *Table 2.1: Architectural Variations of Tarocchi Decks* (regional card counts and features).
* **Forms & Modules**: The *Classic Italian Tarocchi* rulebook layout detailing 3-player configuration point-scoring arrays (120-point system, 5-point Honors, and the specific Wildcard rules of the Fool/The Excuse).
* **Administrative Pages**: Dedicated global footer navigation routing directly to a standalone *AI Disclosure* module and a comprehensive *Bibliography & Citations* directory.

### 4. Tasks
* **What visitors must be able to complete**:
  * **Sequential Reading**: Navigate smoothly through chronological history via a permanent header menu interface.
  * **Data Synthesis**: Analyze complex cross-comparisons between regional decks and literary figures using scrollable responsive tables.
  * **Layout Execution**: Replicate physical layout operations at home (the Daily One-Card pull, the horizontal Past-Present-Future row, and the complex 10-position geometric Celtic Cross matrix).
  * **Sub-Chapter Routing**: Drill down into standalone portfolio nodes using explicit interactive card action link components (`card-action`).

### 5. Constraints
* **Time & Tools**: Developed as a multi-page framework under strict semester guidelines using standards-compliant HTML5 and folder-isolated independent stylesheets.
* **Accessibility Limitations**: Demands strict WCAG 2.1 AA compliance. This requires keyboard-accessible overflow structures (`tabindex="0"`) on data tables, rigorous text-alternative overrides (`alt="..."`) describing complex artwork to screen readers, and heavy color contrast validation on the custom *Emerald Green and Crimson* decorative title banners.
* **Coding Structure Challenges**: The layout makes deep use of inline block nesting (wrapping block-level elements like lists and headers completely inside anchor tags `<a>`). This requires strong CSS reset declarations to override default link behaviors.
* **Performance Limits**: High-resolution graphic inputs require a strict responsive asset configuration pipeline (`srcset` and `sizes` attributes tracking asset resolutions from `480w` up to `1200w`) to ensure pages load quickly on cellular connections.

### 6. Success
* **How you know the site is ready to release**:
  * **Zero Code Violations**: The entire multi-page codebase passes formal W3C HTML5 and CSS validation checks with completely closed tag structures and no console runtime errors.
  * **Flawless Pathing Infrastructure**: Local link auditing verifies that all relative page pathways resolve cleanly without triggering broken links or 404 dead ends.
  * **Responsive Layout Integrity**: Visual verification confirms that all text rows, nested navigation blocks, card grids, and image frames scale cleanly down to mobile screen viewports without letting lists or images bleed or clip past layout containers.
  * **Academic Validation**: The timeline, scoring configurations, and character parallels align perfectly with peer-reviewed historical playing card society records.

---

## 📁 Part 2: Workspace Directory & Style Assignment Map
The design uses `global.css` for universal styling elements (fonts, global colors, resets, footers). To optimize page performance and prevent style bloat, structural layout pages are separated into directories with assigned category-specific stylesheets:

```text
TAROCCHI-TO-TAROT/
├── index.html                   --> Driven by styles/index.css
├── chapter/                     --> Driven by styles/chapter.css
│   ├── one-genesis.html
│   ├── two-mechanics.html
│   ├── three-esoteric.html
│   ├── four-spread.html
│   └── five.frontier.html
├── deck/                        --> Driven by styles/deck.css
│   ├── minchiate-di-firenze.html
│   ├── rider-waite-smith.html
│   └── visconti-sforza.html
├── how-to/                      --> Driven by styles/how-to.css [CSS Pending]
│   ├── play.html
│   ├── read.html
│   └── transcript.html
├── layout/                      --> Driven by styles/layout.css
│   ├── one-card.html
│   ├── three-card.html
│   └── ten-card.html
├── reference-page/              --> Driven by styles/references.css
│   ├── bibliography.html
│   └── disclosure.html
└── styles/
    ├── chapter.css
    ├── deck.css
    ├── global.css
    ├── how-to.css               [⚠️ PENDING WRITING PHASE]
    ├── index.css
    ├── layout.css
    └── references.css
```

---

## 🛠️ Part 3: Active Project Changelog & Progress Tracker

### 📝 [Phase 1] Milestone: Text Baseline & Content Insertion
* **Status**: ⏳ **In Progress**
* **Action Log**:
  * [x] **Core Chapter Tracks**: Main historical text baseline for Chapters 1-5 completely finalized and locked in.
  * [ ] **Auxiliary Sheets**: Compiling, polishing, and finishing the text layers for individual deck description portfolios, rules summary guides, and layout instructions.

### 🔗 [Phase 2] Milestone: Link Normalization & Code Adjustments
* **Status**: ⏳ **In Progress**
* **Action Log**:
  * [ ] **Stylesheet References**: Update file headers to point to category stylesheets instead of the old standalone `page.css`.
  * [ ] **Cross-Folder Path Fixes**: Audit and repair all internal links using the correct relative reference mapping (`../folder/filename.html`) to ensure seamless navigation across nested paths.

### 🎨 [Phase 3] Milestone: Front-End Style Sheets
* **Status**: ⏳ **In Progress**
* **Action Log**:
  * [x] `global.css`: Base tokens, reset, fluid typography parameters, and stationary responsive backgrounds completed.
  * [x] `chapter.css`: Structural text columns, image frame spacing, and container query logic finalized and closed.
  * [x] `deck.css`: 5-column fluid cards grid layout and checkbox click-zoom mechanism completed.
  * [x] `layout.css`: Horizontal multi-card lists, flexbox column distribution rows, and mobile stack overrides completed.
  * [x] `references.css`: High-contrast blockquote boxes and clean academic reference spacing completed.
  * [ ] `how-to.css`: **[PENDING]** Formatting for rules columns, scoring matrices, and instructional text grids.
  * [x] `index.css`: Grid layouts for landing frames completed.

### 🖼️ [Phase 4] Milestone: Image Optimization & Assets Pipeline
* **Status**: 💤 **Planned**
  * [ ] Replace all image tags with high-efficiency `.webp` assets.
  * [ ] Verify that all asset nodes contain correct, descriptive `alt` string values for screen-reader compliance.