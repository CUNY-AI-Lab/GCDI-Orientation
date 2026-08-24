# GCDI Orientation 2026 update checklist

This checklist translates the updated orientation instructions into implementation and verification steps for the HTML slide deck. Slide references below use the original 28-slide order and stable `data-slide` identifiers so that newly inserted slides do not cause later work to drift.

## Source baseline

- [x] Confirm the canonical checkout: `/Users/milwright/Projects/dev/gcdi-cail/gcdi-orientation-2026`.
- [x] Confirm a clean `main` branch before synchronization.
- [x] Run a fast-forward-only pull from `origin/main`; local `HEAD` and `origin/main` are both `d3d844c` (`Already up to date`, 2026-08-24).
- [x] Read the full native Google Doc, not only extracted prose: [GCDI Orientation 2026](https://docs.google.com/document/d/1LbE9tifmJ4hQaI40B-wSfx01n2O7htQ_cnhvshbgcd4/edit).
- [x] Record the Doc version used for implementation: modified `2026-08-24T19:28:15.682Z`, revision `AIroW34nCZlkz6c28BE42-78hh6aVXjmLyiAUf9CiPf2BoPvNfzbHiZwT7Hxj7lC7IrlmmvSFxEqWtguePO3fP0cx8srhmOD8ID-GhE7PS0`.
- [x] Inventory the Doc's 14 embedded image objects (13 unique images) and map each image to its adjacent instruction.
- [x] Verify the direct Digital Fellows Linktree destination: `https://linktr.ee/GCDigitalFellows`.
- [x] Verify that the old PDIG short links are broken or misdirected and use the replacement site shown in the Doc: `https://digitalgrants.commons.gc.cuny.edu/`.
- [x] Inspect the supplied `/Users/milwright/Desktop/GC Orientation.pptx` Manifold source deck. Use source slide 2 (“Featured Projects”) and source slide 7 (“My Application: Passion Project + Open Class”) as the two required replacements. Native slide ID `g3f845ce52fd_0_43` maps to source slide 8, but per the user's later direction, exclude that “Thank you!” slide along with the title/introduction material; leave the other detailed application slides available but unused because they are not required for the two-slide orientation slot.

## Source-to-slide implementation checklist

- [x] `intro-goals` (Doc “Slide 1”): replace “Establish the GC as a leader in digital scholarship” with “GC Digital Initiatives established in 2012 to provide leadership in digital scholarship.”
- [x] `degrees` (original slide 6): change “Linguistics” to “Computational Linguistics.”
- [x] `degrees` (original slide 6): append “Digital Humanities and Data Analysis and Visualization (Advanced Certificate — anticipated 2027).”
- [x] `courses` (original slide 7): change the second column heading from “Data Analysis & Data Science” to “Data Analysis & Visualization.”
- [x] Insert `data-quilt` immediately after `courses`: title it “Speaking Truth to Power Via a Data Quilt,” use the supplied image without distortion, and provide specific alt text.
- [x] `dsl-lab` (original slide 9): replace the old Fellows screenshot with the supplied current Fellows image and update the alt text to match the visible roster.
- [x] `dsl-workshops` (original slide 10): remove the apostrophe from “Digital Fellows’ Workshops.”
- [x] `dsl-workshops`: replace the four workshop rows with the exact supplied Fall 2026 schedule:
  - [x] Tools of Digital Humanities — Tuesday, September 8, 12–1:30 PM, Zoom.
  - [x] A Scholar's Introduction to Git and GitHub — Wednesday, September 16, 2–3:30 PM, Room 7414.
  - [x] Introduction to R — Thursday, September 24, 4–5:30 PM, Room 7414.
  - [x] Introduction to GIS — Tuesday, September 29, 10–11:30 AM, Zoom.
- [x] `dsl-workshops`: include the Digital Fellows Linktree as a visible, working link and use the supplied Linktree QR image without crowding the schedule.
- [x] `dsl-dri` (original slide 11): replace the old image with the supplied current GC Digital Research Institute screenshot and update alt text.
- [x] `dsl-hours` (original slide 13): remove the two outdated posters and use the supplied 2026 Open House postcard.
- [x] `dsl-hours`: include “Open House — Tuesday, September 15, 12–3 PM, Digital Scholarship Lab, Room 7414.”
- [x] `dsl-hours`: remove “on your schedule,” describe consultations as scheduled at a mutually selected time, and link `https://cuny.is/gcdi-consults`.
- [x] `ai-guidelines`: use the newly supplied guidelines/programming QR image and preserve its decoded destination.
- [x] `commons` (original slide 20): retain the platform overview and add the supplied Commons statistics in a readable, non-stretched treatment.
- [x] Insert `commons-cv` after `commons`: explain profiles/CVs and use the supplied Commons profile screenshot.
- [x] Insert `commons-courses`: explain teaching/course uses and use the supplied courses screenshot.
- [x] Insert `commons-groups`: explain connection and collaboration through groups and use the supplied groups screenshot.
- [x] Insert `commons-sites`: explain project/publication sites and use the supplied site screenshot.
- [x] `manifold` and `manifold-oer` (original slides 21–22): replace only the two required source slides—source slide 2 for Featured Projects and source slide 7 for the passion-project/open-class examples. Extract all three source PNGs losslessly and display them with `object-fit: contain` so their 2048×1317, 2048×1446, and 2048×1518 aspect ratios remain intact.
- [x] `grants` and `grants-samples` (original slides 23–24): replace the broken short link with `https://digitalgrants.commons.gc.cuny.edu/`.
- [x] `grants`: replace the old site screenshot with the newly supplied PDIG site screenshot and update alt text.
- [x] `gcdi-fifth-floor` (original slide 27): remove the inaccurate fifth-floor/Data Lab framing and replace it with source-faithful language: DATA Labs have been run on Zoom; Office Hours are hosted in the Digital Scholarship Lab on the seventh floor and on Zoom; dates and times are forthcoming.
- [x] Update README slide count/structure after additions.
- [x] Update versioned CSS/JS asset URLs after all HTML/CSS/JS changes so GitHub Pages does not serve stale behavior.

## Operational to-do list

1. [x] Copy only the supplied images actually used by the deck into `images/`, retain their intrinsic dimensions, and give them stable descriptive filenames.
2. [x] Implement text/link replacements against stable `data-slide` identifiers, not ordinal selectors.
3. [x] Add the data-quilt and Commons slides using existing accessible slide patterns; keep all meaning-bearing screenshot content visible with `object-fit: contain`.
4. [x] Add concise, image-specific alt text and useful `aria-label` values for every new or replaced visual.
5. [x] Reconcile the implementation against every checkbox above; use only the two required Manifold source slides, exclude introduction/thank-you material, and do not import optional application slides.
6. [x] Run structural checks: `git diff --check`, JavaScript syntax validation, unique `data-slide` IDs, valid image paths, valid local anchors, and current slide-counter initialization.
7. [x] Serve the deck locally and verify the flow: deck loads → each changed slide renders → keyboard/scrubber navigation advances to the expected slide → contextual links update → image lightbox opens and closes.
8. [x] Audit every slide at desktop `1280×720` and mobile `390×844`: no slide, `.content`, or `.stage` overflow; no clipping; no unintended scrolling; no unreadable wrapping; no distorted screenshots.
9. [x] Check console warnings/errors and missing image/network requests.
10. [x] Capture focused rendered evidence for the data quilt, updated DSL sequence, expanded Commons sequence, grants update, revised Office Hours/DATA Labs slide, and at least one mobile viewport.
11. [x] Produce a before → after text ledger and retain the complete local `git diff` for review.
12. [x] Present the local changes, QA evidence, completed Manifold replacement, and remaining risks to the user.
13. [x] **Release gate: do not commit, push, trigger GitHub Pages, or claim the live deck is updated until the user explicitly approves publication.**
14. [ ] After approval only: commit, push to `origin/main`, wait for terminal GitHub Pages success, and verify the live slide deck and interactions independently of local QA.

## Definition of done before approval

- [x] Every actionable Doc instruction is implemented from the available source material.
- [x] Every supplied image used in the deck is correctly mapped, readable, undistorted, and described accessibly.
- [x] All changed links resolve to their intended current destinations.
- [x] Desktop and mobile all-slide overflow checks pass with zero offenders.
- [x] Focused interaction and console checks pass.
- [x] The local diff and before → after ledger are ready for user review.
- [x] GitHub remote and live Pages remain unchanged pending explicit approval.
