# Planning Package: Tarocchi to Tarot

---

## 1. Project Brief & Scope

### 1.1 Project Purpose & Concept
**Tarocchi to Tarot: A History of Card Reading** is an archival digital humanities project exploring the historical evolution of Tarot decks. The project maps out how these cards transitioned from an exclusive 15th-century Italian parlor game (*Tarocchi*) to dynamic frameworks for contemporary psychoanalysis, ultimately highlighting their modern technical role as visual training datasets for generative machine learning models.

### 1.2 Target Audience & Personas
*   **Primary Audience:** Cultural history students, digital humanists, and academic researchers tracking printing history, gaming history, and traditional iconographies.
*   **Secondary Audience:** Contemporary web designers and AI researchers looking closely at how classic public-domain artwork translates across responsive layouts and visual classification systems.

### 1.3 Core User Tasks
*   **Linear Chronological Reading:** Browse six sequential history chapters via a consistent global navigation menu without layout fatigue.
*   **Archival Gallery Exploration:** Access optimized imagery, historic context, and structured metadata for three classic target decks.
*   **Accessible Media Interactivity:** Watch external rule walkthroughs while maintaining complete offline access to detailed alternative text transcripts.

### 1.4 Technical Scope & Pivot Control
*   **HTML Structure:** Production semantic HTML5 engines (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer*>`).
*   **CSS Architecture:** Fully custom layout file splitting (`global.css`, `layout.css`, plus scoped page configurations) utilizing CSS Grid components alongside inline Flexbox rows. No external frameworks are applied.
*   **Scoped Layout Reduction:** A strategic design pivot was made to drop live, interactive structural modules for three-card, one-card, and Celtic Cross spreads. The original experimental drafts are safely isolated inside `do-not-use-layouts/`. This pivot limits layout clutter, prevents breaking media wraps on small viewports, and guarantees strict layout performance under tight production schedules.

---

## 2. Content Inventory Matrix

| Content ID | Item / Component | Format | Engineering Source | Status | Risk / Mitigation |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **CN-01** | Primary Site Navigation | HTML Nav List | `index.html` (Global Component) | Complete | Sticky tap-targets overlapping headers; handled via min-touch targets. |
| **TX-01** | Six-Chapter Historical Copy | Text Elements | `chapter/*.html` files | Complete | Wall-of-text fatigue; mitigated by explicit margins and consistent subheaders. |
| **IM-01** | Brand Logo Vector Asset | SVG Image | `assets/illuminated-t.svg` | Complete | Scalability shifts; managed via precise percentage aspect scaling in layout styles. |
| **GL-01** | Visconti-Sforza Gallery Pack | Asset Deck Folio | `assets/visconti-sforza/` | In Progress | Image file bloat; optimized through targeted image compression workflows. |
| **GL-02** | Minchiate di Firenze Pack | Asset Deck Folio | `assets/minchiate/` | In Progress | Uncommon visual assets; verified against open digital archives. |
| **GL-03** | Rider-Waite Smith Pack | Asset Deck Folio | `assets/rider-waite-smith/` | In Progress | Copyright limits; verified 1909 release baseline in the public domain. |
| **VD-01** | Gale Sal Tarocchi Video Portal| Component Link | `index.html` to YouTube target | Complete | Dynamic link failure; insulated by including an offline text-only transcript sheet. |

---

## 3. Site Map & Semantic Page Requirements

### 3.1 Synchronized Directory Tree Map
```text
TAROCCHI-TO-TAROT/
├── index.html
├── planning-package.md
├── assets/
│   ├── minchiate/
│   ├── rider-waite-smith/
│   ├── visconti-sforza/
│   └── illuminated-t.svg
├── chapter/
│   ├── five-spreads.html
│   ├── four-tarot.html
│   ├── one-origins.html
│   ├── six-today.html
│   ├── three-classic.html
│   └── two-anatomy.html
├── decks/
│   ├── minchiate.html
│   ├── rider-waite-smith.html
│   └── visconti-sforza.html
├── do-not-use-layouts/
│   ├── one-card.html
│   └── three-card.html
├── reference-pages/
│   ├── ai-disclosure.html
│   ├── bibliography.html
│   └── video-transcript.html
└── style/
    ├── chapter.css
    ├── deck.css
    ├── global.css
    ├── index.css
    ├── layout.css
    └── reference.css
```

### 3.2 Semantic Landmark Mapping
*   **Root Document (`index.html`):** Anchors layout using `<main class="main-index" id="index-page">` which acts as the grid engine parent for three isolated landmark modules: `#site-description`, `#gallery-nav`, and `#video-nav`.
*   **Narrative Folders (`chapter/`):** Styled uniformly via `style/chapter.css`. All six sub-pages utilize semantic `<article>` wrappers to host linear text blocks.
*   **Deck Showcases (`decks/`):** Controlled via `style/deck.css`, presenting optimized grid configurations for display rows accompanied by descriptive image alt values.
*   **Reference Engines (`reference-pages/`):** Hosts clean, tabular layouts (`<table>`) for project research data citations alongside standard layout streams for reading transcripts.

---

## 4. Responsive Wireframes

### 4.1 Narrow Layout (Mobile: `< 480px`)
```text
+------------------------------------------+

| [T] Tarocchi to Tarot... (Header Block)  |
+------------------------------------------+

| [=] MENU (Stacked 1-Column Links)        |
| - Origins                                |
| - Tarocchi                               |
| - Play                                   |
| ...                                      |
+------------------------------------------+

| MAIN CONTENT WRAPPER                     |
|                                          |
| [#site-description]                      |
| Intro narrative tracking historical      |
| evolution from parlor games to AI.       |
|                                          |
| [#gallery-nav]                           |
| - Visconti Sforza Deck                   |
| - Minchiate di Firenze Deck              |
| - Rider-Waite Smith Deck                 |
|                                          |
| [#video-nav]                             |
| Gale Sal Video Link & Transcript Bridge  |
+------------------------------------------+

| FOOTER (Vertical Stack Layout)           |
+------------------------------------------+
```

### 4.2 Medium Layout (Tablet: `481px - 1024px`)
```text
+------------------------------------------+

| [T] Tarocchi to Tarot | History (Logo-L)  |
+------------------------------------------+

| Origins | Tarocchi | Play | Tarot | ...  |
+------------------------------------------+

| MAIN GRID WRAPPER (2-Column Variant)     |
| +--------------------------------------+ |
| | [#site-description] Full Width Block | |
| +--------------------------------------+ |
| +-----------------+  +-----------------+ |
| | [#gallery-nav]  |  | [#video-nav]    | |
| | Three decks     |  | YouTube link    | |
| | flex list       |  | & transcript    | |
| +-----------------+  +-----------------+ |
+------------------------------------------+

| FOOTER (Inline Items Wrap)               |
+------------------------------------------+
```

### 4.3 Wide Layout (Desktop: `> 1025px`)
```text
+-------------------------------------------------------------------------+

| [T] Tarocchi to Tarot | A History of Card Reading (Inline Layout)       |
+-------------------------------------------------------------------------+

| Origins   ·   Tarocchi   ·   Play   ·   Tarot   ·   Spreads   ·   Today |
+-------------------------------------------------------------------------+

| MAIN CONTENT WRAPPER (`main.main-index` 3-Column Grid)                  |
|                                                                         |
| +-------------------+ +-----------------------+ +---------------------+ |
| | #site-description | | #gallery-nav          | | #video-nav          | |
| |                   | |                       | |                     | |
| | Project summary   | | Deck Navigation       | | External video      | |
| | tracking historical| | - Visconti Sforza     | | resource path &     | |
| | trajectories.     | | - Minchiate di Firenze| | access transcript   | |
| |                   | | - Rider-Waite Smith   | | anchor.             | |
| +-------------------+ +-----------------------+ +---------------------+ |
|                                                                         |
+-------------------------------------------------------------------------+

| [T Logo]      © 2026 Sarah Moore      Bibliography      AI Disclosure   |
+-------------------------------------------------------------------------+
```

---

## 5. Behavior Annotations

### 5.1 Layout Reflow Mechanics
*   **Global Navigation Structure:** The `.site-nav-list` container alters its behavior depending on screen size. For small touch screens, it drops all flex limitations and defaults to a stacked vertical column block. This forces touch target spaces out to a minimum size of **44x44px** to ensure easy interactions. On tablet and desktop screens, it uses `display: flex; justify-content: space-around;` to arrange navigation items horizontally.
• Home Page Columns: The primary layout block (main.main-index) maps content columns dynamically. Desktop viewports run a strict structural rule (display: grid; grid-template-columns: repeat(3, 1fr); gap: 2rem;), laying out description text, galleries, and video portals side-by-side. Tablet viewports condense this down to an asymmetric layout, while mobile screens collapse the grid entirely into a simple one-column vertical block layout.

### 5.2 Element Interactive States
• Focus Ring Overrides: Text link components across the entire platform explicitly protect keyboard interactions. Default outline wipes are restricted; active elements apply a distinct highlight state on both :hover and :focus triggers to keep focus indicators clear.
• Transcript Redirection Component: The specific selector anchor inside #watch-tarocchi a points users straight to our internal document page reference-pages/video-transcript.html. This layout configuration handles media fallback scenarios smoothly, ensuring accessibility even if video streams fail to load.

---

## 6. Project Acceptance Criteria

### 6.1 WCAG 2.2 AA Accessibility Compliance
• Minimum Color Contrast: Text and background layers must maintain a minimum contrast ratio of 4.5:1 for default body text copy and 3:1 for large heading labels.
• Keyboard Accessibility: The entire site must be navigable without a mouse. All functional components must handle focus rings cleanly; interactive links can never hide focus indicators.
• Semantic Element Strategy: Content images must provide accurate alternate descriptions (alt="..."), while decorative graphics must use blank attributes (alt="") so modern screen readers know to skip over them.

### 6.2 Target Performance Metrics
• Largest Contentful Paint (LCP): Core visual elements must render within a maximum target time window of 2.5 seconds.
• Cumulative Layout Shift (CLS): Unexpected content movement must be kept under an index score of 0.1 by defining hard aspect ratios on all visual image files and custom grid containers.

### 6.3 Target Environments
• Cross-Browser Uniformity: Layout rules must perform consistently across Google Chrome, Mozilla Firefox, and Apple Safari.
• Document Meta Standards: Document head tags must include correct language declarations (en-US), charset rules (UTF-8), and proper viewport settings to prevent scaling bugs on mobile devices.

---

## 7. AI Disclosure Statement

### 7.1 Intended Use Cases
AI tools were used exclusively to organize structural file inventory records and cross-check matching path references inside our technical Planning_Package.md document based on the code setup from index.html.

### 7.2 Verification and Modifications
AI recommendations for complex layout options (such as interactive three-card templates) were deliberately removed to keep the site architecture clean and readable. Every folder path and file reference was double-checked against our project file explorer layout before packaging the code for submission.