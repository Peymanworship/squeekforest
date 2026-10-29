# SQUEEKFOREST 🌲🐹

> **Every block plants a story.** An unofficial living pixel forest powered by the Squeekchain Sepolia public API.

Created by **[@AhoteSpirit](https://x.com/AhoteSpirit)**. GitHub maintained at **[@Peymanworship](https://github.com/Peymanworship)**.

## What it does

- Renders an original procedural pixel forest in a lightweight browser canvas.
- Uses the official read-only Squeekchain API: `/v1/core` for **settled Squeek block height** and `/v1/status` for WHEELY9000 **hardware telemetry**.
- Unlocks additional trees every 60 confirmed Squeek blocks within a grove; the next grove begins after 1,200 blocks.
- Lets viewers download a still of the forest as a PNG.
- Treats missing, simulated, replayed or stale telemetry explicitly; no fabricated live readings.
- Works without API keys, wallet connections, contracts, NFT holdings or transactions.

**Demo status:** initial web prototype. The remote API must still be tested end to end on the deployed public URL; this is not a verified Genesis Builder submission.

## Start

Open [`index.html`](./index.html) in a browser. To share a public version, deploy the contents of this repository as a static website using GitHub Pages or another static host. No build step required.

For local development (optional):

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Data fidelity

| Value | API | Meaning |
|---|---|---|
| Settled blocks | `/v1/core` | Confirmed state of SqueekCore on Ethereum Sepolia after the API's safety confirmations |
| Speed / RPM / distance | `/v1/status` | Device measurement, shown as fresh hardware only when provenance, timestamps and freshness criteria pass |
| Grove and tree count | Derived from confirmed Squeek block height | Visual metaphor, not a Squeekchain protocol quantity |

Status and settlement are **not the same stage**: a freshly spinning wheel can be ahead of onchain settlements.

The remote API is still under development, and a successful HTTP request may contain `status: unavailable`. The website avoids representing unknown data as zero. Data freshness on the screen is based on the received hardware measurement timestamp, not just request time.

Docs: https://docs.squeekchain.com/developers/api/

## Why this is different

Instead of yet another token price dashboard, SQUEEKFOREST turns a tangible physical signal (the hamster running on its wheel) into a living public landscape. Its permanent growth depends on **settled chain evidence**, while its motion depends on **fresh hardware readings**.

## Genesis / badge submission

At the time of this prototype, the official Genesis website described the **Buildooooor** badge as “Submit one project with verified attribution,” and Code submissions had not opened. A GitHub repository or a public demo alone **does not guarantee** a badge or whitelist spot. Always check the current official rules at https://squeekchain.com/genesis.

## Security

The site only fetches public, read-only endpoints. It has no wallet connect button and asks for no seed phrase, private key or payment. Do not send sensitive credentials to anyone claiming to be a reviewer.

## Attribution

- Original independent community experiment by **AhoteSpirit**.
- Uses public API data from Squeekchain; not affiliated with or endorsed by Squeekchain.
- License: not assigned yet. Please request permission before reusing the source code.
