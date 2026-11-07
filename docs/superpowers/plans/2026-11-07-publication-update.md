# Publication Website Update Implementation Plan

> Execute the user-approved update inline, using the existing static sites and GitHub Pages repositories.

**Goal:** Synchronize the personal homepage, RoboLineage, and Geometric Entropy with their camera-ready papers.

**Architecture:** Keep each site's existing HTML/CSS and assets. Host the final PDFs on the project sites, retain version-independent arXiv links, and link the personal publication entries to both.

**Tech Stack:** Static HTML/CSS/JavaScript, Python/Pillow for source-figure crops, GitHub Pages.

**Spec:** Approved conversation: fourth-year PhD, RoboLineage CoRL 2026, Code on the project site and personal entry, no extra code disclaimers, current camera-ready PDFs and factual experimental results.

## Constraints

- Preserve older publication entries, including contribution markers.
- Preserve source-image proportions and labels; use original figures and rollout frames.
- Keep simple Code links. No unverified Geometric Entropy repository or release promise.
- Use RoboLineage's 47-page final PDF and Geometric Entropy's final 8-page PDF.
- Do not invent proceedings metadata, DOI, presentation awards, or causal claims.

## Review Focus

- Every local PDF, image, video, anchor, and downloadable slide resolves.
- Paper downloads match the selected final PDFs, not cached arXiv v1.
- Review accuracy, rejected-rollout leakage, diagnostic rounds, final tests, and active human time retain their correct denominators and scope.
- Narrow screens contain tables and navigation without page-level overflow.
- Old publication HTML is unchanged and source figures are not stretched or clipped.

## Tasks

- [x] RoboLineage: CoRL venue, final PDF, full-workflow narrative, review results, precise effort numbers, and final recollection tests; retain Code and existing demonstrations.
- [x] Geometric Entropy: final PDF and affiliation, alignment/metric explanation, mastery interpretation, paper-backed diagrams, citation, and downloadable presentation.
- [x] Personal homepage: fourth-year, research sentence, CoRL venue, final paper/arXiv/code links, and naturally proportioned thumbnails.
- [x] Validate resources, source values, legacy entries, PDF contents, desktop/mobile rendering and gallery interaction; obtain an independent review.
- [ ] Commit and push each site; verify deployed HTML and PDF hashes.

## Execution Notes

- Work in the existing user-selected repositories. The user explicitly approved updating and pushing them; no additional worktree or publishing approval is needed.
- These are static content and asset changes. Use focused resource/content validation and browser QA rather than introducing a test framework.
- The replacement submission may precede the public arXiv announcement. Local final PDFs remain the authority for this release.
- Resource/content checks pass for all sites. The 11 legacy publication rows are unchanged. Hosted PDFs match the selected source SHA256 hashes and contain 47 and 8 pages.
- Browser checks at 360, 390, 768 and 1280 pixels find no page-level horizontal overflow or broken images. The qualitative gallery switches both by mouse and keyboard.
- Independent review identified overgeneralized Geometric Entropy claims; these now distinguish measured settings from the mastery/ambiguity interpretation.
- Read-only slide audit: the October 31 RoboLineage PPTX retains old table images and differs from the final paper. It is not part of this publication update and remains untouched.
