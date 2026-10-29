# Deployment and QA notes — SQUEEKFOREST

**Current deployment (as checked 29 Oct 2026):** GitHub Pages is serving the `main` branch from the repository root.

- **Demo:** https://peymanworship.github.io/squeekforest/
- **Source:** https://github.com/Peymanworship/squeekforest
- **HTML entrypoint:** `index.html`
- **Current UI version:** v0.3

## Updating the project

1. Update the desired file in the repository. On mobile, choose **Add file → Upload files** and select files inside the extracted archive, not the ZIP archive itself.
2. If a file already exists with the same name at the root, uploading the replacement to the same path replaces that file when committed.
3. Commit directly to `main`. GitHub Pages deploys changes from `main` and `/(root)`.
4. Reopen the public demo; use a clean query string like `?v=3` if the browser still displays cached HTML.
5. Verify that core data and other content render before publicly describing the update as complete.

## Tested on the live site

On 29 October 2026, the live site was opened on Android and visibly displayed `2,994` settled Squeek blocks, `GROVE 03`, and `9/20` trees. The official core endpoint independently returned `core.blockHeight = "2994"`. This is an observation from that day, not a statement about the current block height.

## What still needs testing

- A successful network refresh with a changed settled block height
- API outage, timeout and 429 behavior
- Stale, simulated and unavailable hardware states
- Desktop usability across browsers, keyboard accessibility, and slow-network handling

## Builder workflow

Code submissions were not open when this dossier was prepared. See [`BUILDER_SUBMISSION.md`](./BUILDER_SUBMISSION.md). Re-check https://squeekchain.com/genesis before any official submission. A live GitHub Pages site is **not** evidence that the team has verified or whitelisted the creator.
