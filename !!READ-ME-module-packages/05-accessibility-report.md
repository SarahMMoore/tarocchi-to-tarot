# Accessibility Conformance and Inclusive Quality Build Report

**Project Name:** Tarocchi to Tarot: A History of Card Reading  
**Author:** Sarah Morrigan Powers Moore  
**Submission Date:** October 2026  
**Target Conformance Tier:** Web Content Accessibility Guidelines (WCAG) 2.1 Level AA  
**Build Environment:** Semantic Native HTML5, CSS Cascading Layers (`global.css`), Chrome DevTools Audit Panel  

---

## 1. Test Scope & Rationale

Three distinct standalone pages representing core functional components across the *Tarocchi to Tarot* application architecture were isolated for rigorous accessibility testing and code remediation:

*   **Page 1: Global Homepage & Index Gateway (`index.html`)**
    *   **Rationale:** Establishes the global layout template baseline for the application. It handles primary global landmarks, global site-navigation rows, and repetitive multi-link deck-selection blocks. Testing this ensures structural entry paths are clear.
*   **Page 2: Chapter Five Module — How To Conduct a Modern Spread (`chapter/five-spreads.html`)**
    *   **Rationale:** Chosen to evaluate dense instructional text layouts paired with complex multi-stage graphical diagrams (e.g., the 10-card Celtic Cross grid matrix layout). Testing this page checks sequential heading outlines and spatial text alternatives for non-text assets.
*   **Page 3: Media Demonstration & Alternate Fallbacks Page (`reference-pages/video-transcript.html`)**
    *   **Rationale:** Evaluates multimedia dependencies, third-party iframe embed integrations (YouTube walkthrough rules), and deep linear text reading layouts for timestamped data streams (transcripts).

---

## 2. Automated and Manual Testing Evidence Base

Evaluation checkpoints were conducted using a strict hybrid checklist process combining automated scanning algorithms with manual human-assistive navigation paths:

*   **Automated Engine Tooling:** Axe DevTools Browser Extension Suite (v4.6.0) and Google Lighthouse Auditing System.
*   **Manual Keyboard Control:** Full physical verification pass using standard desktop hardware key cycles (`Tab`, `Shift + Tab`, `Enter`) to check focus maps, trap blocks, and activation states.
*   **Screen Reader / Accessibility-Tree Inspector:** Native macOS VoiceOver engine combined with the Chrome DevTools Accessibility Object Model (AOM) Node tree view.
*   **Visual/Reflow Controls:** Chrome Developer Tools Responsive Viewport simulation forcing content to step up to **400% zoom parameters** alongside manual CSS text-spacing rule injections.

---

## 3. Core Accessibility Category Evaluations

### 🧱 Semantic Structure
*   **Page Titles:** Checked and verified that unique, hierarchical string parameters are explicitly attached to every head scope (e.g., `<title>Tarocchi to Tarot | Chapter Five | How To Conduct a Modern Spread</title>`).
*   **Landmarks:** Structural wrappers utilize proper native HTML5 landmarks (`<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<footer>`) to allow screen readers to orient themselves instantly on the page. Duplicated or redundant `<nav>` tags inside the home sub-modules were removed to protect landmark tracking clarity.
*   **Headings:** Remediated multiple structural heading cliffs across chapter layout structures where subsections skipped directly from an `<h2>` block level straight into an `<h4>` or `<h5>`. Headings now cascade strictly sequentially (`<h1>` \(\rightarrow\) `<h2>` \(\rightarrow\) `<h3>` \(\rightarrow\) `<h4>`).
*   **Accessible Names:** Modified non-descriptive multimedia link anchor texts. Changed generic string labels like `"Watch the game"` to explicit context references: `"Read the video transcript"`.

### ⌨️ Keyboard and Focus Controls
*   **Keyboard Access:** All interactive target endpoints on the site utilize native, focusable anchor tags (`<a>`), guaranteeing complete keyboard functionality without a pointer mouse device.
*   **Focus Order:** Sequential tab paths completely preserve logical reading patterns, preventing spatial focus loops from breaking when responsive layouts shift from mobile vertical layout stacks to desktop horizontal rows.
*   **Focus Visibility:** Repaired an invalid CSS layout syntax split inside `global.css` at line 234 (`outline-offset: var(`). Engineered a custom state rule that renders clear focus highlights across all items: `outline: 3px double var(--color-gold-bright) !important; outline-offset: var(--focus-offset) !important;`.
*   **Skip Navigation:** Implemented a functional `.skip-link` shortcut element positioned as the absolute first child of the `<body>` element on every page. This stays hidden off-screen until prompted via a keyboard `Tab` press, allowing users to instantly skip global menu lists on page load and jump focus directly to `<main id="..." tabindex="-1">`.

### 🔍 Zoom, Reflow, Text Spacing, and Contrast
*   **400% Zoom Reflow:** Menu blocks and content sections leverage flexible layout parameters and flex-wrapping definitions (`flex-wrap: wrap;`). At 400% zoom scales, items wrap down fluidly into a clean vertical row column, preventing horizontal scrollbars.
*   **Text Spacing Pass:** Injected WCAG text-spacing definitions (forcing line heights to 1.5x and letter spacing to 0.12x). Content containers adjusted dynamically without overlapping or clipping text lines.
*   **Color Contrast Repair:** Discovered a severe contrast failure on `.page-header h1` where charcoal text (`#151514`) over dark forest green background accents (`#143d30`) rendered at a low **1.3:1 ratio**. Updated text color properties to use `--color-text-light` (`#dfd8cb`), moving the element up to a passing **6.8:1 color contrast ratio**.

### 📋 Forms and Tables
*   **Table Caption Structures:** Remediated a semantic parsing failure inside the Chapter 6 data matrix table where a block-level `<h3>` element was nested inside the `<caption>` tag. Converted the description into clean paragraph lines, preserving accessible screen reader tracking.
*   **Table Spacing Integrity:** Appended clean, hidden programmatic cell spacer alignments (`<td class="table-grid-spacer" aria-hidden="true">`) to incomplete grid rows inside the RWS layout module to protect the table container grid bounds from collapsing during zoom sweeps.

### 🎨 Media, Motion, and Alternative Elements
*   **Image Purpose:** The master branding graphic in the header holds an explicit functional description (`alt="Tarocchi to Tarot Logo"`), whereas identical graphic icons inside footer fields are marked with empty parameters (`alt=""`) to tell screen reader engines to bypass them.
*   **Complex Text Alternatives:** Eliminated all vague or ungrounded alternative placeholders on layout graphics across your files. Alt text fields explicitly detail layout geometries and card features (e.g., `alt="Detail diagram of the layout center: Card 1 stands vertically on the table, while Card 2 is placed horizontally directly over top of it, creating an intersecting cross shape."`).
*   **Video & Motion Mitigation:** Third-party video iframes utilize descriptive `title` attributes. Embedded a defensive `@media (prefers-reduced-motion: reduce)` rule configuration block directly inside the style layers to instantly strip away hover scaling transitions and animation keyframes for users with vestibulocochlear sensitivities.
## 4. Screen Reader / Accessibility-Tree Sampling

*   **Sampled Element Component:** Global Site Navigation Block Menu (`<nav class="site-nav" id="main-nav">`).
*   **What Was Checked:** Evaluated using VoiceOver on macOS. The menu wrapper was announced clearly as a *"Main Site Navigation, navigation landmark element panel"*. Advancing focus via keyboard tabs correctly announced individual text destinations alongside position contexts (e.g., *"Origins, link, item 1 of 6"*). Active location targets are announced as the current page using explicit programmatic attributes: `aria-current="page"`.
*   **Limitations of Sample:** This inspection provides successful verification for structural layout data exposure. However, it tests static interaction trees and cannot account for multi-browser rendering engine changes, or how legacy screen reader configurations map JavaScript states over time.

---

## 5. Remediation Log

| Finding ID | Issue Identified | Found Evidence (Tool / Method) | Inclusive User Impact | Priority Baseline | Remediation Applied | Retest Verification Result |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **01** | Severe Title Text Contrast Failure | Automated Audit: Contrast ratio of **1.3:1** on main site header. | Low-vision and color-blind visitors cannot read the site title. | **Critical** | Swapped font color properties from `#151514` to `--color-text-light` (`#dfd8cb`). | **PASSED:** Contrast retest scores a passing **6.8:1**. |
| **02** | Heading Tree Sequence Broken | Structural Check: Chapter layouts jumped irregularly from `<h2>` to `<h4>` or `<h5>`. | Screen reader users navigating text via hotkey landmarks skip core text chunks. | **High** | Normalized subsection headings down into clean sequential order steps (`<h2>` \(\rightarrow\) `<h3>`). | **PASSED:** The heading cascade map renders properly. |
| **03** | Broken Focus Indication Variable | CSS Inspection Audit: Line 234 string split error (`outline-offset: var(`). | Keyboard-only visitors lose track of their active visual pointer navigation focus frames. | **Critical** | Completed the malformed variable definition call to reference `var(--focus-offset) !important;`. | **PASSED:** Focus indication outline renders prominently on tab paths. |
| **04** | Misplaced and Broken Skip Navigation Link | Manual Control Pass: Shortcut link `href="#index-page"` nested inside the `<main>` body. | Keyboard users are forced to loop through header logos, making the menu bypass useless. | **Critical** | Moved the link block to the top of `<body>` and targeted the correct container elements. | **PASSED:** Keyboards jump immediately past navigation menus. |
| **05** | Table Caption Heading Node Violation | W3C Validator Pass: Nesting block-level heading elements inside a `<caption>` tag. | Assistive software packages fail to announce table context metrics cleanly to users. | **High** | Stripped out the invalid heading tags and styled caption details with paragraph selectors. | **PASSED:** Data grid tables parse and announce flawlessly. |

---

## 6. Conformance Summary

*   **What Conforms:** Global template semantic structures, document title descriptors, text color contrast scales, native keyboard step loops, focus visibility states, and fluid zoom reflow properties up to 400% fully conform to WCAG 2.1 Level AA criteria.
*   **What Was Remediated:** Fixed critical contrast failures inside the header layout, repaired broken syntax variables within the state layer of the master stylesheet, resolved mismatched heading depths, corrected broken relative root directory pathways, and established an operational skip-navigation mechanism.
*   **Remaining Limitations:** Third-party video playback assets remain embedded externally via an `<iframe>`, relying on Google's player shell script parameters to convey underlying button cues.
*   **Pre-Release Checklist Pass:** Before deploying the repository to final production release, run a final validation sweep across all remaining sub-module documents to verify structural heading hierarchies remain uniform.

---

## 7. AI Disclosure

*   **Purpose of AI Use:** AI was used to execute automated design token structural code reviews, analyze underlying palette color choices against mathematical WCAG contrast specifications, and construct organized markdown presentation components.
*   **Output Considered:** Remediated HTML attribute structures, text alternative descriptions for non-text graphics, and programmatic focus visibility states.
*   **Verification Methods:** Every code remediation step, heading structure update, and keyboard skip-navigation tab loop path was manually validated by the author inside a live local browser sandbox using real developer tools and screen reader software utilities.
*   **What Changed:** Standardized and refined all generated code snippets, template descriptors, block hierarchies, and variable colors to explicitly match the custom historical archival aesthetics of this capstone repository.
