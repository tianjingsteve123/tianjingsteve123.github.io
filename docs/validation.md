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
