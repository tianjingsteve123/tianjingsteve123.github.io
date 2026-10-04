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

Deployment and public-site verification are recorded below after publishing.
