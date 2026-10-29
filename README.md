# SQUEEKFOREST 🌲🐹

> **Every block plants a story.** A living pixel forest driven by verified Squeekchain Sepolia data.

**[OPEN THE LIVE DEMO](https://peymanworship.github.io/squeekforest/)** · **[EXPLORE THE SOURCE](https://github.com/Peymanworship/squeekforest)** · **[OFFICIAL API DOCUMENTATION](https://docs.squeekchain.com/developers/api/)**

Created as an **independent community experiment** by **[@AhoteSpirit](https://x.com/AhoteSpirit)**, published from the GitHub account **[@Peymanworship](https://github.com/Peymanworship)**. This is **not** an official Squeekchain app or an endorsed product.

## What it is

SQUEEKFOREST transforms Squeekchain's hamster-powered physical work into a digital forest. Every **60 settled Squeek blocks** unlocks another tree in the current grove, and every **1,200 settled blocks** begins a new chapter. These visual thresholds are **artistic choices**, not protocol rules.

The forest reads the **official, public, read-only API**:

| Input | Endpoint | Role |
| --- | --- | --- |
| Settled Squeek block height | [`GET /v1/core`](https://api.squeekchain.com/v1/core) | Drives grove number and tree growth |
| WHEELY9000 wheel telemetry | [`GET /v1/status`](https://api.squeekchain.com/v1/status) | Drives movement only when measurement provenance and freshness checks pass |

The site distinguishes **onchain-settled blocks** from **new, potentially unsettled hardware measurements**. It does not present simulations, stale readings, or unavailable data as verified live hardware. If confirmed chain state is unavailable, no substitute block height is invented.

No tokens, wallet connection, contract transactions, API keys, or payments are needed to view the forest.

## Live prototype: v0.3

- **Public site:** https://peymanworship.github.io/squeekforest/
- **Source:** [`index.html`](./index.html), a lightweight, self-contained HTML/CSS/JavaScript app (no build step).
- **Mobile verification:** On **29 October 2026**, a mobile browser session loaded the live GitHub Pages site and displayed **2,994 settled Squeek blocks**, **GROVE 03**, and **9/20** new trees. The user also independently opened the official `/v1/core` endpoint and observed that same block height. These numbers are a **dated snapshot**, not claimed current values.
- **Video evidence:** A short raw mobile walkthrough and a separate edited product introduction exist and can be provided to reviewers; they are not treated as proof of official approval.
- **Known limits:** The API is under development. Live refreshes may not change the counter if no new blocks settle. Long-term uptime, cross-browser behavior, failure scenarios, and continuously changing live data have not been independently certified.

## See it working

1. Open the [public demo](https://peymanworship.github.io/squeekforest/).
2. Note the **Confirmed Squeek Blocks** counter and grove label.
3. Open the [official SqueekCore response](https://api.squeekchain.com/v1/core) separately and compare the **`core.blockHeight`** field. Copy the endpoint exactly: it rejects unknown query parameters.
4. Select **SYNC REAL DATA** in the demo. The refresh can legitimately return the same block height.
5. Scroll through the mechanism explanation and use **SAVE THE FOREST** to export a still of the forest.

## Data integrity and safety

- Both API endpoints are accessed over HTTPS. The site validates the expected API schema, Sepolia chain ID and EVM-format core address before displaying the settled height.
- The API's published address can change between testing deployments; the app reads the current identity dynamically instead of pinning an outdated address.
- Absent, stale, and non-hardware telemetry must not be portrayed as confirmed live activity.
- Block height is a Squeekchain-derived quantity; it is not the Ethereum L1 block height.
- This is **view-only**. Never send a seed phrase or private key to someone claiming to verify this project.

The authoritative technical reference is the [Squeekchain API documentation](https://docs.squeekchain.com/developers/api/).

## Genesis Builder attribution

SQUEEKFOREST was created as a prospective submission for **the Buildooooor badge**. The [official Genesis page](https://squeekchain.com/genesis) describes that badge as requiring **one project with verified attribution**. As checked on **29 October 2026**, the **Code submission path was not open**. This project **has not been submitted, accepted, or awarded a Builder badge or whitelist spot**.

- **Creator's public X identity:** [@AhoteSpirit](https://x.com/AhoteSpirit)
- **Public GitHub owner:** [@Peymanworship](https://github.com/Peymanworship)
- **Deployed demo:** https://peymanworship.github.io/squeekforest/
- **Reviewer notes:** [`BUILDER_SUBMISSION.md`](./BUILDER_SUBMISSION.md)

Final eligibility, attribution verification, and submission requirements must be checked against official Genesis rules when the Code pathway opens.

## Run locally

Download this repository and open `index.html` directly in a browser. For local development, you can also serve it using:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Rights

The app and narrative are an original independent community contribution. It uses public, read-only data from Squeekchain. No open-source license is granted yet; contact the author before republishing the source. Neither Squeekchain nor its team has endorsed or reviewed this project.
