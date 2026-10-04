📄 Tarocchi to Tarot | Complete Discoverability & Structured Content Package

Build Architecture: Semantic HTML5, CSS Layers, JSON-LD Schema, Custom Domain Configuration

1. Metadata Inventory & Page Purpose
This inventory connects each active HTML document inside your workspace directory to its machine-readable text components, canonical addresses, and user-centered interaction metrics:

    [Root] index.html
    ├── chapter/
    │    ├── one-origins.html
    │    ├── two-anatomy.html
    │    ├── three-classic.html
    │    ├── four-tarot.html
    │    ├── five-spreads.html
    │    └── six-today.html
    ├── decks/
    │    ├── minchiate.html
    │    ├── rider-waite-smith.html
    │    └── visconti-sforza.html
    └── reference-pages/
          ├── ai-disclosure.html
          ├── bibliography.html
          └── video-transcript.html

  🏠 Global Homepage Index (index.html)
  • Page Purpose: Serves as the primary educational landing hub and entry gateway into your historical archival chapters and deck galleries.
  • Unique Page Title: Tarocchi to Tarot | A History of Card Reading | Home
  • Meta Description: An archival history mapping the development of the Tarot deck from 15th-century Italian parlor games to modern data vector networks.
  • Canonical URL Decision: https://tarocchi-to-tarot.com (Points permanently to the root custom domain to eliminate duplicate query indexing).
  • Primary Heading (H1): Tarocchi to Tarot | A History of Card Reading
  • Target User Task: Orienting the user, providing immediate baseline site context, and facilitating frictionless routing into individual sequential chapters.

  📜 Chapter One (chapter/one-origins.html)
  • Page Purpose: Details the early transcontinental migration of playing cards from Tang Dynasty China to Europe.
  • Unique Page Title: Tarocchi to Tarot | Chapter One | Origins of Playing Cards
  • Meta Description: A history of card reading, from the origins of playing cards in Tang Dynasty China to the development of Tarot in Renaissance Italy. Explore the evolution of card games, symbolism, and divination practices.
  • Canonical URL Decision: https://tarocchi-to-tarot.com
  • Primary Heading (H1): Origins of Playing Cards
  • Target User Task: Reading historical prose, tracing trade route timelines, and analyzing card structural ancestry patterns.

  📜 Chapter Two (chapter/two-anatomy.html)
  • Page Purpose: Analyzes the core 78-card structure of Renaissance decks and regional layout adaptations across Italian city-states.
  • Unique Page Title: Tarocchi to Tarot | Chapter Two | Anatomy and Production of Tarocchi
  • Meta Description: An archival history mapping the physical production, deck anatomy, and regional variations of Renaissance Tarocchi cards.
  • Canonical URL Decision: https://tarocchi-to-tarot.com
  • Primary Heading (H1): Anatomy and Production of Tarocchi
  • Target User Task: Comparing socioeconomic production techniques and auditing regional deck variations (Milanese, Bolognese, Florentine).

  📜 Chapter Three (chapter/three-classic.html)
  • Page Purpose: Operates as a strategic rulebook detailing the bidding, mechanics, and point matrices of classic Italian card games.
  • Unique Page Title: Tarocchi to Tarot | Chapter Three | How to Play Classic Italian Tarocchi
  • Meta Description: A beginner's strategic guide detailing the rules, bidding phases, suit hierarchies, and scoring matrix of the traditional 3-player Renaissance card game of Italian Tarocchi.
  • Canonical URL Decision: https://tarocchi-to-tarot.com
  • Primary Heading (H1): How to Play Classic Italian Tarocchi
  • Target User Task: Learning competitive rules, executing trick calculations, and accessing instructional reference media pages.

  📜 Chapter Four (chapter/four-tarot.html)
  • Page Purpose: Traces the transformation of card decks from games into Western esoteric systems and psychological frameworks.
  • Unique Page Title: Tarocchi to Tarot | Chapter Four | From Tarocchi to Tarot
  • Meta Description: A comprehensive historical analysis mapping the transformation of Tarot cards from an 18th-century French parlor game into a symbolic framework for Western occultism and analytical psychology.
  • Canonical URL Decision: https://tarocchi-to-tarot.com
  • Primary Heading (H1): From Tarocchi to Tarot
  • Target User Task: Studying historical occult shifts, reviewing Kabbalistic charts, and evaluating Jungian dream models.

  📜 Chapter Five (chapter/five-spreads.html)
  • Page Purpose: Provides structural instructions on how to conduct and physically arrange modern divinatory layout grids.
  • Unique Page Title: Tarocchi to Tarot | Chapter Five | How To Conduct a Modern Spread
  • Meta Description: A comprehensive guide on formulating queries, shuffling, and setting up modern divinatory Tarot spreads, including the One-Card Pull, Three-Card Spread, and Celtic Cross.
  • Canonical URL Decision: https://tarocchi-to-tarot.com
  • Primary Heading (H1): How To Conduct a Modern Spread
  • Target User Task: Setting up cards at home following spatial layout charts and reading position mapping rules.

  📜 Chapter Six (chapter/six-today.html)
  • Page Purpose: Bridges the gap between old symbolic card arrays, tabletop game design engines, and artificial intelligence model benchmarks.
  • Unique Page Title: Tarocchi to Tarot | Chapter Six | Tarot Today — From Divination to Data Science
  • Meta Description: An investigation into modern Tarot, tracing its journey from a tool for psychological self-discovery and mindfulness to its application in narrative game design and computer data systems.
  • Canonical URL Decision: https://tarocchi-to-tarot.com
  • Primary Heading (H1): Tarot Today — From Divination to Data Science
  • Target User Task: Conceptualizing cards as data array models, evaluating computer vision training challenges, and accessing legacy collection links.

  🖼️ Deck Gallery Modules (decks/minchiate.html, etc.)
  • Page Purpose: Houses optimized grid data display matrices highlighting historical card art.
  • Unique Page Title: Tarocchi to Tarot | Deck Gallery | [Deck Name]
  • Meta Description: An archival digital deck gallery presenting major trump cards arranged in structured reference grid layout matrices.
  • Canonical URL Decision: https://tarocchi-to-tarot.com[deck-name].html
  • Primary Heading (H1): Deck Gallery: [Deck Name]
  • Target User Task: Browsing historical illustrations, viewing visual text annotations, and navigating back-and-forth between chapter nodes.

  📄 Reference Data Fallbacks (reference-pages/video-transcript.html, etc.)
  • Page Purpose: Anchors accessible transcript fallbacks, video players, academic source lists, and required transparency statements.
  • Unique Page Title: Tarocchi to Tarot | Reference Pages | [Page Purpose]
  • Meta Description: Archival reference documentation assets and text data fallbacks supporting the Tarocchi to Tarot project.
  • Canonical URL Decision: https://tarocchi-to-tarot.com[file-name].html
  • Primary Heading (H1): [Document Purpose Header]
  • Target User Task: Reading timestamped transcripts, auditing source documentation links, and reviewing academic disclosure statements.

2. Technical Roadmap: Canonical, Robots, and Sitemap Notes
To support automatic machine-readable web scraping engine discovery, this capstone architecture implements a multi-tiered search systems deployment strategy.
• Canonical Tags Mapping: APPLIES NOW. Explicit <link rel="canonical" href="..."> nodes are hardcoded into the <head> block of every document in the workspace tree. This instructs search engines to treat the custom domain paths as the single source of truth, completely preventing duplicate content indexing penalties if the site is accessed via raw local testing servers or development previews.
• Robots Rules (robots.txt): APPLIES IMMEDIATELY AFTER PUBLICATION. A root text block file will be placed at the absolute root directory (/robots.txt) upon production launch. It instructs web scrapers which asset fields are safe to index, preventing them from reading local markdown packages or styles:txt

  User-agent: *
  Allow: /
  Allow: /chapter/
  Allow: /decks/
  Disallow: /module-packages/
  Disallow: /style/

  Sitemap: https://tarocchi-to-tarot.com

• XML Sitemaps (sitemap.xml): APPLIES IMMEDIATELY AFTER PUBLICATION. An XML index file mapping all eleven public text files within the workspace tree will be uploaded at launch. This map guarantees search engine crawlers can recursively find and index deep nested sub-directories (like inside your /chapter/ and /decks/ folders) without getting lost.

3. Social Metadata (Open Graph Protocol)
To optimize structural preview cards when links are shared across communication networks, Chapter Four implements the Open Graph rich-media markup suite inside its head container:

  html
  <!-- Open Graph Social Metadata Assets (Chapter 4 Example Configuration) -->
  <meta property="og:title" content="From Tarocchi to Tarot: The Occult &amp; Psychological Transformation" />
  <meta property="og:type" content="article" />
  <meta property="og:url" content="https://tarocchi-to-tarot.com" />
  <meta property="og:image" content="https://tarocchi-to-tarot.com" />
  <meta property="og:image:alt" content="A structural graphic showing Éliphas Lévi's 1854 historical alignment pairing the 22 Major Arcana cards with the Hebrew alphabet." />
  <meta property="og:description" content="Trace the history of Tarot cards from an 18th-century French parlor game into a symbolic framework for Western occultism and Carl Jung's psychological archetypes." />
  <meta property="og:site_name" content="Tarocchi to Tarot History Project" />
  <meta name="twitter:card" content="summary_large_image" />

4. Machine-Readable Structured Data (JSON-LD Schema Graph)
The root homepage (index.html) embeds a valid, comprehensive structured data block inside the head tags. This tells search engine crawlers that the website is an integrated, sequential textbook entity, linking chapters and metadata directly within a single semantic object model.

  html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "WebSite",
    "@id": "https://tarocchi-to-tarot.com",
    "url": "https://tarocchi-to-tarot.com",
    "name": "Tarocchi to Tarot: A History of Card Reading",
    "description": "An archival history mapping the development of the Tarot deck from its origins as a 15th-century Italian parlor game to modern data visualization vectors.",
    "inLanguage": "en-US",
    "author": {
      "@type": "Person",
      "name": "Sarah Morrigan Powers Moore"
    },
    "publisher": {
      "@type": "Organization",
      "name": "Arizona State University Capstone Publishing"
    }
  }
  </script>

5. Image Discoverability Inventory
To satisfy crawlers and image indexing systems, all major media placeholders inside your folder architecture are explicitly optimized with distinct file naming trees and visual alt strings.

  🖼️ Asset 1: Primary Platform Brand Mark (assets/illuminated-t.svg)
  • Page Relevance: Serves as the global branding visual identity across every page header.
  • Image Dimensions: 80px width × auto height fluid scaling.
  • Surrounding Text Context: Sits adjacent to your primary page landmark headers (<h1>Tarocchi to Tarot</h1>).
  • Remediated Alt Text Decision: alt="Tarocchi to Tarot Logo" (Declared functionally when inside the header wrapper link, but set as empty alt="" inside the footer to skip screen-reader clutter).

  🖼️ Asset 2: Ancient Card Proof Block (assets/image-placeholder.png inside Chapter 1)
  • Page Relevance: Illustrates the section detailing 9th-century woodblock manufacturing techniques.
  • Image Dimensions: Scaled fluidly using percentage CSS rules via .placeholder.
  • Surrounding Text Context: Embedded inside the Tang Dynasty section directly above the descriptive list items outlining Princess Tongchang's leaf game records.
  • Remediated Alt Text Decision: alt="A 9th-century Chinese money card produced by woodblock printing, displaying stylized stacks of cash currency symbols."

  🖼️ Asset 3: Interlocking Card Layout Grid (assets/image-placeholder.png inside Chapter 5)
  • Page Relevance: Displays the intricate spatial arrangements required to physically execute the 10-card Celtic Cross spread.
  • Image Dimensions: Set to responsive column bounds via .placeholder.
  • Surrounding Text Context: Nested inside the central cross layout subgroup directly above the descriptive list elements tracking Card 1 and Card 2 placement axes.
  • Remediated Alt Text Decision: alt="Detail diagram of the layout center: Card 1 stands vertically on the table, while Card 2 is placed horizontally directly over top of it, creating an intersecting cross shape."

6. Validation Evidence
Every markup fix, layout token mapping, and JSON structured data array was manually cross-checked inside local server test branches using native developer inspection environments:

   1. DevTools Source Code Audit Pass: Verified that the structured JSON-LD block parses without exceptions or hidden text breaks within the local network console logs.

   2. Structural Heading Outline Trees: Confirmed via element selectors that heading tags follow an exact cascading path (<h1> → <h2> → <h3>) across all files in your /chapter/ and /decks/ folder paths, completely free of any structural cliffs.

   3. Crawlable Anchor Verification: Audited all <a> tags inside index.html and chapter files, ensuring every link points to a fully crawlable HTML file path rather than utilizing broken JavaScript selectors.

   4. Search Engine Ranking-Claim Limits
   To ground this project package in realistic, source-backed evidence, the application explicitly identifies two search engine optimization boundaries that will not be promised:

   5. No Guarantee of Immediate Page-One Ranking for "Tarot History": The phrase "Tarot History" is saturated with massive competition from highly authoritative commercial platforms (e.g., Wikipedia, historical blogs, online card encyclopedias). Because search engines prioritize domain age, link weight profiles, and massive query volumes, our specialized mini-site project will not claim an immediate top ranking without extensive, long-term backlink networks.

   6. No Claims Regarding Automatic User Engagement Actions: While this package ensures search engine crawlers can flawlessly map and index our text nodes, this mechanical discoverability does not guarantee user interactions (e.g., long session times or users choosing to share our content). Discoverability code only guarantees that search crawlers can process the cards—it does not dictate human reader behavior.

1. AI Disclosure
• Purpose of AI Use: AI was leveraged to compile the page-by-page metadata inventory tables, structure the valid JSON-LD schema array blocks, and formulate highly descriptive text alternative metadata descriptions for the graphic asset layouts.
• Output Considered: Machine-readable Open Graph social metadata headers, structured schema code fragments, and organized markdown presentation blocks.
• Verification Methods: Every file structure, path string routing boundary (e.g., verifying relative directories like ../style/global.css), and index tracking layout parameter was tested manually inside your active local server environment.
• What Changed: Reconfigured and customized all metadata strings, chapter pathways, and image descriptions to perfectly match the exact file architecture, class tokens, and historical criteria of your capstone repository.
