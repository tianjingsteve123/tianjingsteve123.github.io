# Release verification

Verified October 4, 2026, against the actual static site in Chrome via agent-browser 0.38.1.

- Desktop: 1440 × 1000 viewport; full page inspected.
- Mobile: 390 × 844 and 320 × 740 viewports; screenshots inspected. No horizontal overflow at either width. Portrait and essay photograph load.
- Keyboard: the first Tab exposes “Skip to content”; Enter moves focus to the `main` element and updates the fragment to `#main`.
- Research, Writing, and About navigation: each click reaches its exact fragment. Native anchor scrolling avoids interrupted smooth-scroll clicks.
- Kīlauea essay link: clicked in the browser; reached the published English essay with its expected title.
- Accessibility: axe-core 4.12.1 reported 41 passing checks, zero violations, and zero incomplete checks in the final desktop audit. This automated check is not a complete accessibility certification.
- External links: all three publication destinations, GitHub, and the two essay languages returned HTTP 200. Scholar was read successfully for identity and publication verification, then rate-limited a later automated link check with HTTP 429. LinkedIn returns HTTP 999 or its login gate for automated public requests. Their stable profile URLs remain the destinations; the access limits are not presented as broken links or bypassed.
- Privacy: the publish directory contains no private account analytics, personal email addresses, credentials, or pasted profile export. Biography is based on the owner's supplied career information. Both 2026 preprints are labeled explicitly; no academic degree or lead-author role is inferred.

## Public deployment

- Live root: https://tianjingsteve123.github.io/ returned HTTP 200. The delivered HTML SHA-256 was `23291dbaf6410743424e798ff0d203b7ebae10875bc3b4e683cd8c559e237017`, identical to the locally inspected release.
- Initial release commit: `cfcf9269f28539dbd2743c610bb570c668e8ff5c`. GitHub identifies both its author and committer as `tianjingsteve123`.
- [Initial Pages deployment](https://github.com/tianjingsteve123/tianjingsteve123.github.io/actions/runs/37197116445) completed successfully.
- The public root was opened in Chrome and inspected at 1440 × 1000 and 390 × 844. At mobile width, document width equals viewport width, both images load, and no resource reports an HTTP error. The live axe audit again reports zero violations and zero incomplete checks.
- GitHub's contribution collection includes the homepage repository and its initial commit. Existing Kīlauea English and Chinese destinations still return HTTP 200.

## Career, publication and reading-layout update

The October 4 update adds the owner's Cedars-Sinai and Neusoft Medical records and expands Selected research to seven publications. Publisher equal-contribution text supports the first item's co-first-author label. A complete 71-record Scholar snapshot supports the dated highest-cited second item. Radiology and IEEE JBHI metadata agree between publisher-deposited Crossref records and PubMed. The original European Radiology tuberculosis article and both digital-biology preprints remain, with the journal articles first and both preprint labels retained.

Local Chrome inspection at 1440 × 1000 and 390 × 844 confirmed the seven-item order, both new career rows, loaded images and readable linked titles. At 320px and 390px, document width equals viewport width with no horizontal overflow. The final local axe audit reports zero violations and zero incomplete checks. The Background text is capped at 65ch and research titles at 34em; warm-paper colors, portrait and image widths are preserved.

The updated release is commit `69e48c2b75cf6e8f7cbf904c767bcefccbef9cff`; its [Pages workflow](https://github.com/tianjingsteve123/tianjingsteve123.github.io/actions/runs/37198511899) succeeded. The public root returned HTTP 200 with HTML SHA-256 `799be2f55492d16b307e1faabb6179df8c6ee82c11d2d42bf6259ca2d4a36e0d`, identical to the locally inspected page. Browser inspection on the public domain confirmed all seven titles in the requested order, Cedars-Sinai's Research Associate II record, the underlined title links and the narrower Background text. The live axe audit reports zero violations and zero incomplete checks.

## Responsive reading refinement

The next refinement stacks career dates above company and role text on phones, increasing the description width from 172 to 280px at a 320px viewport and from 242 to 350px at 390px. Supporting type is slightly larger. Tablet introduction and section content use the available reading width, with fluid outer gutters; the original 600/601px research-column drop from 560 to 387px is now a continuous 552/553px. Desktop research begins at approximately 525px, 31px earlier than before. The warm-paper palette, Georgia headings and both photographs are retained.

Independent Chrome inspection covered 1440, 390 and 320px, plus 600/601, 800/801 and 900/901px. Screenshots of the introduction, all research, writing and background were inspected. None showed horizontal page overflow, clipped text or overlap. The 900/901px change introduces the desktop section rail while keeping long publication titles readable.

All 21 links were traversed with Tab at 1440 and 320px. Visible focus and the skip link were checked; Enter on Research, Writing and About reached their expected fragments. Axe-core 4.12.1 returned zero violations and zero incomplete checks at 1440, 390 and 320px. Console and page-error outputs were empty. These are Chrome checks with simulated viewports, not physical-device or comprehensive accessibility certification. Native 200% page zoom was attempted but did not change the browser state and remains unverified.

The entire body is identical to the prior release except for the Kīlauea image's intrinsic height correction to its actual 2200×1650 file size. All publication titles, metadata and order, all seven career rows, and all link destinations are unchanged. The stylesheet URL now includes its content hash to avoid serving a cached pre-refinement stylesheet after publication. Public deployment is verified separately after this local release is committed.
