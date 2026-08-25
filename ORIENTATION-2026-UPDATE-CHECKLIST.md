# GCDI Orientation 2026 update checklist

This checklist translates the updated orientation instructions into implementation and verification steps for the HTML slide deck. Slide references below use the original 28-slide order and stable `data-slide` identifiers so that newly inserted slides do not cause later work to drift.

## Source baseline

- [x] Confirm the canonical checkout: `/Users/milwright/Projects/dev/gcdi-cail/gcdi-orientation-2026`.
- [x] Confirm a clean `main` branch before synchronization.
- [x] Run a fast-forward-only pull from `origin/main`; local `HEAD` and `origin/main` are both `d3d844c` (`Already up to date`, 2026-08-24).
- [x] Read the full native Google Doc, not only extracted prose: [GCDI Orientation 2026](https://docs.google.com/document/d/1LbE9tifmJ4hQaI40B-wSfx01n2O7htQ_cnhvshbgcd4/edit).
- [x] Record the Doc version used for implementation: modified `2026-08-24T19:28:15.682Z`, revision `AIroW34nCZlkz6c28BE42-78hh6aVXjmLyiAUf9CiPf2BoPvNfzbHiZwT7Hxj7lC7IrlmmvSFxEqWtguePO3fP0cx8srhmOD8ID-GhE7PS0`.
- [x] Re-read Matt's additive second-round update at Drive revision `4158`, modified `2026-08-24T23:55:18.380Z`; confirm revision `3211` is the immediate prior version, the first-round requests remain unchanged, and no embedded image changed.
- [x] Re-read the updated outline section for Tagging the Tower from revision `AIroW340zNsaHN0Vcqn4hiTMwgmoSkgeBVz92UV1icAyZ5BD1aO8UflNV6mTSG33dDTejtxJ9jFDUWhuF4I89jC-BuJWdEeLq9MqcLxqSf4`; confirm the exact entry `Tagging the Tower || cuny.is/ttt` follows Office Hours.
- [x] Inventory the Doc's 14 embedded image objects (13 unique images) and map each image to its adjacent instruction.
- [x] Verify the direct Digital Fellows Linktree destination: `https://linktr.ee/GCDigitalFellows`.
- [x] Verify that the old PDIG short links are broken or misdirected and use the replacement site shown in the Doc: `https://digitalgrants.commons.gc.cuny.edu/`.
- [x] Inspect the supplied `/Users/milwright/Desktop/GC Orientation.pptx` Manifold source deck. Per the user's final explicit sequence, use source slides 2, 4, 5, 6, and 7 in that order, followed by the existing “Open Education Projects & Workshops” orientation slide. Exclude source slide 1 (title), source slide 3 (introduction/biography/contact), and source slide 8 (“Thank you!”/workshop/contact close).

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
- [x] Insert `tagging-tower` immediately after `dsl-hours`: use the supplied 2602×1962 screenshot without cropping or distortion, add no slide copy, and expose only `cuny.is/ttt` through the existing deck-link treatment.
- [x] `ai-guidelines`: use the newly supplied guidelines/programming QR image and preserve its decoded destination.
- [x] `commons` (original slide 20): retain the platform overview and add the supplied Commons statistics in a readable, non-stretched treatment.
- [x] Insert `commons-cv` after `commons`: explain profiles/CVs and use the supplied Commons profile screenshot.
- [x] Insert `commons-courses`: explain teaching/course uses and use the supplied courses screenshot.
- [x] Insert `commons-groups`: explain connection and collaboration through groups and use the supplied groups screenshot.
- [x] Insert `commons-sites`: explain project/publication sites and use the supplied site screenshot.
- [x] Expand the Manifold section in the required order: source slide 2 (`manifold`), source slide 4 (`manifold-reading-groups`), source slide 5 (`manifold-journals`), source slide 6 (`manifold-projects`), source slide 7 (`manifold-applications`), then `manifold-oer`. Retain every required image and relationship while making the user-directed layout concession: use the orientation deck's shared title/body scale and content/image structure rather than rigid PowerPoint mirroring. Match the Commons opener with label “Platforms” and title “Manifold Scholarship”; label the five follow-up slides “Manifold”; keep every screenshot at `object-fit: contain`.
- [x] `grants` and `grants-samples` (original slides 23–24): replace the broken short link with `https://digitalgrants.commons.gc.cuny.edu/`.
- [x] `grants`: replace the old site screenshot with the newly supplied PDIG site screenshot and update alt text.
- [x] First-round `gcdi-fifth-floor` revision (original slide 27): remove the inaccurate fifth-floor/Data Lab framing and replace it with source-faithful DATA Labs/Office Hours language. This historical state is superseded by second-round item 29 below.
- [x] Update README slide count/structure after additions.
- [x] Update versioned CSS/JS asset URLs after all HTML/CSS/JS changes so GitHub Pages does not serve stale behavior.

## Operational to-do list

1. [x] Copy only the supplied images actually used by the deck into `images/`, retain their intrinsic dimensions, and give them stable descriptive filenames.
2. [x] Implement text/link replacements against stable `data-slide` identifiers, not ordinal selectors.
3. [x] Add the data-quilt and Commons slides using existing accessible slide patterns; keep all meaning-bearing screenshot content visible with `object-fit: contain`.
4. [x] Add concise, image-specific alt text and useful `aria-label` values for every new or replaced visual.
5. [x] Reconcile the implementation against every checkbox above; include source slides 2, 4, 5, 6, and 7, exclude source slides 1, 3, and 8, and retain a distinct final Open Education Projects & Workshops slide.
6. [x] Re-run structural checks for the 37-slide correction: `git diff --check`, JavaScript syntax validation, unique `data-slide` IDs, valid image paths, valid local anchors, and current slide-counter initialization.
7. [x] Serve the corrected deck locally and verify the flow: slide 25 → source slides 2, 4, 5, 6, and 7 → Open Education Projects & Workshops → grants; confirm contextual links and image lightbox behavior.
8. [x] Re-audit every corrected Manifold slide at desktop `1280×720` and mobile `390×844`: no overflow, clipping, unintended scrolling, unreadable wrapping, cropping, or distorted screenshots.
9. [x] Re-check console warnings/errors and missing image/network requests.
10. [x] Capture focused rendered evidence for the complete six-slide Manifold sequence at desktop and mobile sizes.
11. [x] Produce a before → after text ledger and retain the complete local `git diff` for review.
12. [x] Present the corrected local sequence and QA evidence to the user.
13. [x] The user approved and the initial 33-slide implementation was published as commit `e158b92`; GitHub Pages run `32776095038` completed successfully. The later in-window review showed that its two-slide Manifold interpretation was too narrow.
14. [x] **Correction release gate:** user explicitly approved the corrected version for publication on 2026-08-24 (“Push this update and fix manifold pronto”).
15. [x] Commit and push the correction as `fddc415`; wait for GitHub Pages run `32777521621` to finish successfully; then verify the deployed sequence independently at slides 26–31, including exact “Manifold” labels, 37-slide counters, image loading and aspect-ratio containment, Next-button navigation, image lightbox behavior, and an empty browser console.
16. [x] Normalize the local Manifold revision to deck-native typography: remove the 42%-zoom heading structure, move explanatory copy into `.content`, and keep screenshots as supporting evidence.
17. [x] Add the screenshot-only Tagging the Tower slide in outline order with the exact `cuny.is/ttt` shortlink and update the local deck to 38 slides.
18. [x] Verify the revised local Manifold and Tagging slides at `1280×720`, the user's `1071×969` review viewport, and mobile `390×844`; require contained images, bounded text, no slide overflow, working navigation/lightbox behavior, and a clean browser console. Enlarge the two `manifold-applications` screenshots in balanced full-slide project cards, restore each source relationship as project type followed by its distinct “Future Iteration” line, and keep all card copy in the deck's regular-weight body typography without ad-hoc bolding.
19. [x] **New release gate:** the user explicitly approved publication on 2026-08-24 (“push”), then directed the final `manifold-applications` image-size and wording refinements before publication.
20. [x] Replace the `manifold-journals` screenshot with the newly supplied 1962×1956 JITP journals-page image, preserve the prior source asset, update the image-specific accessible description, and change the second bullet exactly to “Look for JITP Issue 30 general call in early fall.”
21. [x] Change the `manifold-projects` title exactly from “Class & Passion Projects” to “Classroom Use and Passion Projects.”
22. [x] Verify the journal replacement and projects title locally; push commit `439a57d`; wait for GitHub Pages run `32781602552` to complete successfully; verify live slides 29–30 for exact text, the 1962×1956 contained JITP image, standard title sizing, zero overflow, and a clean browser console.
23. [x] Remove the `cail-sandbox` request-access secondary header link and access-form QR card while retaining the primary Sandbox link and separate model-registry link.
24. [x] Verify the simplified Sandbox slide locally at `1280×720`, `1071×969`, and `390×844`; the user approved the combined release on 2026-08-24 (“Implement and push”).
25. [x] Leave the existing mix of section-title slides unchanged this round, as explicitly directed.
26. [x] Insert `toc` after `presenters` with the exact seven-part presentation outline from revision `4158`.
27. [x] Change the upper labels on `degrees`, `courses`, and `data-quilt` from “Degree Programs & Certificates” to “Coursework.”
28. [x] Remove only the top-right `dsl-workshops` “Digital Fellows Linktree” contextual link; retain the in-slide Linktree QR and visible URL.
29. [x] Rebuild `gcdi-fifth-floor` as “GC Digital Scholarship Lab,” match the preceding NML two-column visual structure, remove the DATA Labs copy, and use Matt's four exact bullets.
30. [x] Restore `cdsdv` after `gcdi-fifth-floor` from the earlier presentation source using both tracked 1500×1133 architectural renderings without distortion.
31. [x] Change the final slide to “Looking Forward” and update the institution line to “The CUNY Graduate Center.”
32. [x] Verify all 40 slides at `1280×720`, `1071×969`, and `390×844`; update the overview grid/counters/cache keys; push commit `6c99eba`; wait for GitHub Pages run `32803385928` to finish successfully; and verify the live deck's links, navigation, lightbox, 40-tile overview, empty console, image containment, and byte-identical served HTML/CSS/JavaScript.
33. [x] Supersede the earlier screenshot-only treatment by adding the exact visible title “Tagging the Tower Blog”; retain the supplied screenshot and `cuny.is/ttt` shortlink unchanged.
34. [ ] After explicit user approval, push the Tagging the Tower Blog title revision, wait for terminal GitHub Pages success, and verify the live slide independently.

## Definition of done

- [x] Every actionable Doc instruction is implemented from the available source material.
- [x] Every supplied image used in the deck is correctly mapped, readable, undistorted, and described accessibly.
- [x] All changed links resolve to their intended current destinations.
- [x] Desktop and mobile all-slide overflow checks pass with zero offenders after the Manifold expansion.
- [x] Focused interaction and console checks pass after the Manifold expansion.
- [x] The local diff and before → after ledger are ready for user review.
- [x] The corrected 37-slide version is published from `fddc415` and independently live-verified after successful GitHub Pages run `32777521621`.
- [x] The new 38-slide typography and Tagging the Tower revision received explicit publication approval.
- [x] Push the approved 38-slide revision and its final Manifold comparison refinement (`29b7860`, then `6ccea63`); wait for terminal GitHub Pages success (runs `32779679309` and `32780175425`); verify live slide 15 (`tagging-tower`), slide 27 (`manifold`), and slide 31 (`manifold-applications`) for exact text, regular-weight card typography, image containment, counters, zero overflow, and a clean browser console.
- [x] Publish and independently live-verify the final JITP journal image/copy and “Classroom Use and Passion Projects” title revision from `439a57d` after successful Pages run `32781602552`.
- [x] Publish and independently live-verify the approved 40-slide second-round revision from `6c99eba` after terminal GitHub Pages success in run `32803385928`.
- [ ] Publish and independently live-verify the “Tagging the Tower Blog” title revision after explicit approval.
