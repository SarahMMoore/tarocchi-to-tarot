# 📊 Tarocchi to Tarot: Content Inventory & Risk Matrix Audit

This comprehensive specification matrix provides a granular itemized audit of all content nodes, data layout frameworks, responsive graphical assets, and technical directory tracks within the `TAROCCHI-TO-TAROT` site workspace. 

---

## 📂 1. Directory Track: `/chapter/` (Core Chronological Timeline)

### 📄 Item: `one-genesis.html` (Chapter One)
*   **Purpose**: Tracks the non-occult global pre-history of playing cards (from Tang Dynasty paper currency leaves to Mamluk Egypt) and links the structure of Italian trumps directly to the allegorical psychological hierarchies in Petrarch's 14th-century poem *I Trionfi*.
*   **Status**: 🛠️ **Needs Revision**
*   **Owner / Source**: Academic research copy compiled from the International Playing-Card Society archives and Silk Trade customs manifests. 
*   **Format**: Semantically structured text, multi-density responsive visual vectors (`srcset`), and one cross-comparison table container.
*   **Risk Profiles**: 
    *   *Performance*: Heavy pixel-density variations must be properly optimized via custom `.webp` extensions to keep LCP metrics under 2 seconds.
    *   *Technical/Accuracy*: Contains a broken orphan unclosed anchor node (`</a>`) at the tail of the Figure 5 `<figcaption>` description block that must be stripped to prevent layout breakages.
    *   *Licensing*: Demands careful tracking of Creative Commons attributions (`CC BY-SA 3.0` link references) for public domain assets harvested from Wikimedia Commons.

### 📄 Item: `two-mechanics.html` (Chapter Two)
*   **Purpose**: Explains the structural architecture of the 78-card deck (56 suited pip and court elements and 22 un-suited trump pieces) and details the programming short-circuit evaluation design pattern where a trump overrides standard suit rules.
*   **Status**: 🛠️ **Needs Revision**
*   **Owner / Source**: Historical research derived from British Museum playing card catalogs and Renaissance guild records of Italian *cartegiari* (card-makers).
*   **Format**: Text layers, multi-nested itemized list elements, custom grid layout cells, and tabular layouts.
*   **Risk Profiles**: 
    *   *Accessibility*: Table 2.1 introduces a major accessibility breakdown due to a structural column mismatch (the `<thead>` defines 4 header columns while individual rows inside `<tbody>` contain 5 data cells). This distorts screen reader traversal.
    *   *Technical/Accuracy*: Contains unresolved raw textual strings (`TO DO` markers) inside all alt-text property paths and card captions that must be replaced with our descriptive text parameters.

### 📄 Item: `three-esoteric.html` (Chapter Three)
*   **Purpose**: Charts the transition of Tarot cards inside 18th-century French Enlightenment salons from a simple parlor card game into an esoteric map of the subconscious, mapping Court de Gébelin's Egyptian Book of Thoth myth, Etteilla's divination layouts, and Éliphas Lévi's Kabbalistic connections.
*   **Status**: ⏳ **Ready (Text Core)**
*   **Owner / Source**: Text synthesized from historical publication records of Antoine Court de Gébelin (1781) and Éliphas Lévi (1854).
*   **Format**: Dense academic text layers organized via bullet structures and target block-action transition anchors.
*   **Risk Profiles**: 
    *   *Accessibility/Contrast*: The document sets up a critical style override notice at the header: *Pattern 4 Override: Emerald Green Title Banner with Crimson Lip*. This background color block introduces high contrast risks that must be validated under WCAG 2.1 AA text-readability algorithms.

### 📄 Item: `four-spread.html` (Chapter Four)
*   **Purpose**: Maps Carl Jung's analytical frameworks of universal archetypes and the Collective Unconscious to the Major Arcana cards, and charts the technical dealing steps behind the Golden Dawn's historical "Opening of the Key" multi-operation system.
*   **Status**: ⏳ **Ready (Text Core)**
*   **Owner / Source**: Integrated psychological theory records and late 19th-century Hermetic scriptural files ("Book T").
*   **Format**: Text, highly complex multi-tiered nested list trees, and relative path sub-chapter hyperlinks.
*   **Risk Profiles**: 
    *   *Maintenance*: The text layer nests detailed list elements (`<ul>` and `<li>`) completely inside high-utility inline anchor cards (`<a class="card-action">`). To prevent browser font styling distortion or line truncation on small mobile devices, the associated CSS rules inside `layout.css` require specific block resets.

### 📄 Item: `five.frontier.html` (Chapter Five)
*   **Purpose**: Explores how Tarot's rigid mathematical layout mirrors modern relational database models, tracks the utilization of card logic as a narrative plot randomizer engine in game design (D&D), and defines how abstract cards act as a benchmark for testing multimodal AI models.
*   **Status**: 🛠️ **Needs Revision**
*   **Owner / Source**: Sourced from computational logic history (Leibniz's binary derivation from the *I Ching*), game mechanics repositories, and machine learning sentiment-analysis benchmarks.
*   **Format**: Text descriptions, ordered sequential tracking blocks (`<ol>`), and terminal home folder navigation link buttons.
*   **Risk Profiles**: 
    *   *Technical/Accuracy*: The text cuts off mid-word on the final card legacy item (`with ri...`), causing unclosed layout containers that throw compilation faults. This must be populated with the finalized Rider-Waite-Smith paragraph strings.
    *   *Maintenance*: The file name features an accidental period notation anomaly (`five.frontier.html`) rather than a uniform hyphen separator (`five-frontier.html`). This creates a path variance that must match navbar mapping perfectly to avoid dead paths.

---

## 📂 2. Directory Track: `/how-to/` & `/layout/` (System Handbooks)

### 📄 Item: `play.html` (Under `/how-to/`)
*   **Purpose**: Houses the interactive guidebook detailing the gameplay regulations of Renaissance Tarocchi, illustrating long suit progression rules, inverted round suit values, and the wildcard mechanics of the Fool.
*   **Status**: ⏳ **Needs Revision**
*   **Owner / Source**: Traditional rules translated from historic Italian tournament configuration records.
*   **Format**: Informational instruction text, structural card rank lists, and open content container modules.
*   **Risk Profiles**: 
    *   *Technical/Accuracy*: The text block is written but cuts off abruptly at the opening of an asset section container without its terminal main tags, section blocks, or footer layouts attached.

### 📄 Items: `one-card.html` / `three-card.html` / `ten-card.html` (Under `/layout/`)
*   **Purpose**: Independent layout sheets designed to host detailed instructional matrices, workspace alignment criteria, and multi-card radio-driven visual layout grids.
*   **Status**: 🛠️ **In-Progress**
*   **Owner / Source**: Contemporary secular self-discovery and projection methodologies.
*   **Format**: Structural text grids, layout vectors, and interactive element labels.
*   **Risk Profiles**: 
    *   *Maintenance*: The pure CSS click-to-zoom card preview systems depend entirely on native checkbox and radio selector structures. These require identical ID matching between the text files and `layout.css` to prevent image swap failures.

---

## 📂 3. Directory Track: `/reference-page/` (Project Administration)

### 📄 Items: `bibliography.html` / `disclosure.html`
*   **Purpose**: Provides administrative data modules recording full academic bibliography records and the required, ethical course-compliant AI tool disclosure statement.
*   **Status**: 🛠️ **In-Progress**
*   **Owner / Source**: Student-authored validation data.
*   **Format**: Academic citation block lines styled under `references.css` components.
*   **Risk Profiles**: 
    *   *Accessibility*: Fine-print citations and web URLs must use careful text color blocks to guarantee sharp text visibility over aged ivory backgrounds.

---

## 📊 4. Core Directory Style Sheet Mapping & Status Tracker

| Folder Location | Stylesheet Asset File Name | Architectural Responsibility | Current Phase Status |
| :--- | :--- | :--- | :---: |
| Root Level | `index.css` | Handles index layout frames, large double-border box styling, and the asymmetrical grid splits. | ✅ **Finished** |
| `/styles/` | `global.css` | Implements `@layer` resets, typography tokens, color values, and stationary viewport fixed background-image attachments. | ✅ **Finished** |
| `/styles/` | `chapter.css` | Configures multi-column text containers, floating visual figure rules, and responsive table container queries. | ✅ **Finished** |
| `/styles/` | `deck.css` | Manages 5-column item lists, hidden checkbox states, and pure CSS `:has()` cell expansion zoom overrides. | ✅ **Finished** |
| `/styles/` | `layout.css` | Houses responsive radio selector menu cards, image-frame sizes, and horizontal column-reverse tablet realignments. | ✅ **Finished** |
| `/styles/` | `references.css` | Coordinates bibliography block rows, custom list edge lines, and high-contrast (6.5:1 ratio) text definitions. | ✅ **Finished** |
| `/styles/` | `how-to.css` | Controls rulebook data grids, ranking cards, and score computation tracking layouts. | 🛠️ **Pending CSS** |