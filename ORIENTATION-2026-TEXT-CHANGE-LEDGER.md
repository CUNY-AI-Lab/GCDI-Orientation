# GCDI Orientation 2026 text-change ledger

This ledger compares the synchronized GitHub baseline at commit `d3d844c` with the local, uncommitted review version. It is the durable before → after record for text, labels, links, and image descriptions changed while implementing the August 24, 2026 Google Doc instructions.

## Slide text and labels

| Stable slide | Before | Local review version |
| --- | --- | --- |
| `intro-goals` | “Establish the GC as a leader in digital scholarship” | “GC Digital Initiatives established in 2012 to provide leadership in digital scholarship” |
| `degrees` | “Linguistics” | “Computational Linguistics” |
| `degrees` | No corresponding list item | “Digital Humanities and Data Analysis and Visualization (Advanced Certificate — anticipated 2027)” |
| `courses` | “Data Analysis & Data Science” | “Data Analysis & Visualization” |
| `data-quilt` | No corresponding slide | Label: “Degree Programs & Certificates”; title: “Speaking Truth to Power Via a Data Quilt” |
| `dsl-workshops` | “GC Digital Fellows’ Workshops” | “GC Digital Fellows Workshops” |
| `dsl-workshops` | “Tools of Digital Humanities — Monday, September 7 · 12–1:30 PM · Zoom” | “Tools of Digital Humanities — Tuesday, September 8 · 12–1:30 PM · Zoom” |
| `dsl-workshops` | “Introduction to GIS — Information forthcoming” | “Introduction to GIS — Tuesday, September 29 · 10–11:30 AM · Zoom” |
| `dsl-workshops` | No Linktree block | “Workshops, consultations, events, and resources” plus visible `linktr.ee/GCDigitalFellows` link and “Digital Fellows Linktree” header label |
| `dsl-hours` | “Office Hours & Consultations” | “Open House, Office Hours & Consultations” |
| `dsl-hours` | No Open House row | “Open House — Tuesday, September 15 · 12–3 PM · Digital Scholarship Lab, Room 7414” |
| `dsl-hours` | “One-on-one consultations with a Digital Fellow, on your schedule” | “One-on-one consultations with a Digital Fellow at a mutually selected time” |
| `dsl-hours` | No visible consultation URL | `cuny.is/gcdi-consults` |
| `commons-cv` | No corresponding slide | “Academic Profiles & CVs”; “Create a public profile for your academic identity”; “Share research and teaching interests, education, contact links, and a CV”; “Connect your profile to your activity across the Commons” |
| `commons-courses` | No corresponding slide | “Courses”; “Use Commons course sites to support teaching and learning”; “Bring course materials, links, and class activity into one place”; “Discover featured courses from across CUNY” |
| `commons-groups` | No corresponding slide | “Groups”; “Join or create a group around a program, center, method, or shared interest”; “Use activity, forums, events, libraries, and membership tools to collaborate” |
| `commons-sites` | No corresponding slide | “Sites”; “Publish public-facing research, teaching, and institutional projects”; “Build a site within the Commons and connect it to the wider CUNY community” |
| `manifold` | “Manifold @CUNY” | “Manifold @ CUNY” |
| `manifold` | “An intuitive, collaborative, open-source platform for digital publishing”; “Iterative texts, powerful annotation tools, rich media, and reading groups”; “Free for the entire CUNY community” | “Browse original scholarship, teaching handbooks, and collaborative student projects”; “Find customized course versions of public-domain texts and textbooks” |
| `manifold-oer` | “Open Educational Resources, journals, and classroom editions of public-domain texts”; “Original scholarship, teaching handbooks, and collaborative student projects”; “Workshops on building your own Manifold project throughout the year” | “Make a personal passion project public and develop it toward a digital dissertation”; “Build a culminating project for a class at Brooklyn College and carry it forward as a co-created, co-built project for and with K–12 educators”; “Join workshops on building your own Manifold project throughout the year” |
| `gcdi-fifth-floor` | “GCDI on the Fifth Floor”; “365 Fifth Avenue, Suite 5307”; “Data Lab: an informal, interdisciplinary space to discuss all things data”; “Drop-in hours, workshops, consultations, and user groups” | “DATA Labs & Office Hours”; “DATA Labs have previously been run on Zoom”; “Office Hours are hosted in the Digital Scholarship Lab on the seventh floor — Room 7414 — and on Zoom”; “Dates and times forthcoming” |

The Git/GitHub and Introduction to R workshop rows were already correct and their text did not change. The three existing Commons overview bullets also did not change. The supplied Manifold mini-deck contained eight slides; only source slides 2 and 7 were required to replace the two existing Manifold slots. The title/introduction material and “Thank you!” slide were explicitly excluded.

## Links and accessible descriptions

| Location | Before | Local review version |
| --- | --- | --- |
| `dsl-lab` image description | General 2025 Fellows/program description | Names the seven visible 2026 Digital Fellows and notes their disciplines |
| `dsl-dri` image description | “GC Digital Research Institute website: participants work together at a long table full of laptops” | “Current GC Digital Research Institute website with participants working together at a long table full of laptops” |
| `dsl-hours` context link | `https://cuny.is/gcdfconsults` | `https://cuny.is/gcdi-consults` |
| `dsl-hours` slide label | “Office Hours and Consultations” | “Open House, Office Hours, and Consultations” |
| `dsl-hours` images/descriptions | Two separate Office Hours and Student Consultations flyers | One supplied Open House postcard described with its date, time, lab, and room |
| `commons` slide label | “CUNY Academic Commons” | “CUNY Academic Commons overview and statistics” |
| `commons` image description | Homepage-only overview | Separate descriptions for the supplied Commons statistics and the retained homepage image |
| `manifold` context link | CUNY Manifold site | Retains the CUNY Manifold site without importing contact material from the excluded “Thank you!” slide |
| `manifold` image/description | Older Manifold welcome screenshot | Lossless 2048×1317 Featured Projects source PNG, with an image-specific description naming the four fully visible projects |
| `manifold-oer` images/descriptions | Older Featured Projects screenshot | Two lossless project screenshots from source slide 7, shown without cropping or stretching and described separately as the Daniel Simidor project and Brooklyn College open-class project |
| `grants` and `grants-samples` links | `https://cuny.is/pdig` | `https://digitalgrants.commons.gc.cuny.edu/` with visible label `digitalgrants.commons.gc.cuny.edu` |
| `grants` image description | General PDIG program description | Describes the current PDIG site, navigation, news, and featured bilingual youth texting corpus project |
| Slide counter | `1 / 26`, scrubber maximum `26` | `1 / 33`, scrubber maximum `33` |

The AI Guidelines slide has a newly supplied QR image, but its visible text and decoded destination did not change. The data-quilt and four new Commons images each have image-specific alt text in `index.html`.

## README comparison

**Before:** “27 slides following the 2026 orientation outline,” followed by a statement that content and screenshots carried over from the 2025 deck.

**After:** “33 slides following the updated 2026 orientation outline,” an explicit note that the deck adds the Data Quilt and Commons profiles/CVs, courses, groups, and sites slides, and a statement that the deck combines retained 2025 material with the August 24, 2026 instructions and supplied Manifold source deck.

## Non-text implementation changes

- Imported fifteen source images used by the deck, including three lossless PNGs from the supplied Manifold source; omitted the duplicate QR object, optional tall Linktree screenshot, and non-required Manifold slides.
- Added contained Commons composite-image layout and full-stage Sandbox fragment containment.
- Expanded overview grids to hold 33 slides without scrolling.
- Updated matching CSS/JavaScript cache keys to `20260824-manifold`.

For the complete code-level comparison, review the still-uncommitted local diff with:

```sh
git diff -- README.md index.html src/styles.css
```
