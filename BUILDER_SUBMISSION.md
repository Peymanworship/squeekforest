# SQUEEKFOREST — Builder submission dossier

**Prepared 29 October 2026 · Not yet submitted or officially verified**

## One-minute review

- **Product:** SQUEEKFOREST
- **Tagline:** *Every block plants a story.*
- **Category:** Interactive pixel-art data visualization / community-built educational demo
- **Live demo:** https://peymanworship.github.io/squeekforest/
- **Public code:** https://github.com/Peymanworship/squeekforest
- **Creator:** https://x.com/AhoteSpirit
- **Repository owner:** https://github.com/Peymanworship
- **Network:** Squeekchain Sepolia (Ethereum chain ID 11155111)
- **Data:** https://api.squeekchain.com/v1/core and https://api.squeekchain.com/v1/status

## Copy-ready submission text

SQUEEKFOREST is an independent, publicly accessible pixel forest that turns Squeekchain's hamster-powered work into a visual world. Its grove and tree growth are derived from confirmed SqueekCore block height on Sepolia, while fresh, provenance-checked wheel telemetry can influence the forest's movement. Every 60 settled Squeek blocks grows another tree; every 1,200 begins a new grove. Unlike a simulated dashboard, it labels missing or stale data honestly and distinguishes live hardware observations from settled onchain records. The entire app is view-only and works without a wallet or API key. Built by @AhoteSpirit (GitHub: Peymanworship). Demo: https://peymanworship.github.io/squeekforest/ · Source: https://github.com/Peymanworship/squeekforest

## Proof for reviewers

1. Open the demo in a mobile or desktop browser. Inspect the grove, counter, interaction and provenance language.
2. Open https://api.squeekchain.com/v1/core and compare `core.blockHeight` with **Confirmed Squeek Blocks** on the demo; allow for API refresh and settlement timing.
3. Press **SYNC REAL DATA** and note that an unchanged height is valid between settlements.
4. Review source code in `index.html`. Check that both HTTP requests are read-only, that correct network/schema checks are made and that error values are not silently replaced by invented counts.
5. Verify creator attribution in this README, the public project footer and the connected X account.

## Actual recorded evidence

- **29 Oct 2026**: screenshot of running Github Pages application with `2,994` confirmed blocks, `GROVE 03`, `9/20` trees.
- User independently inspected the public API and saw matching `core.blockHeight = "2994"`, `status = "available"`, and Sepolia chain ID `11155111`.
- Short raw mobile screencast (~20 seconds), showing the public demo. An edited 40-second music-backed product film is also available separately.
- These captures are historical proof of the observed presentation, **not** of continuing uptime, new settlement activity, or official approval.

## Key disclosure

This is a read-only API-based visual experience, **not** a new smart contract deployed by @AhoteSpirit. Its acceptance as a Builder contribution is **not confirmed**. The official Genesis Code application, verification method and eligibility criteria must be checked at submission time. Public source and creator credit by themselves may be insufficient for verified attribution; the team may request an additional signed or public ownership proof.

## Submission checklist

- [x] Public project and public source
- [x] API-backed onchain-settled block height displayed in real mobile browser
- [x] Mobile screenshot and screencast captured
- [x] Source explains input data and failure states
- [x] README and footer credit creator
- [ ] Official Code submission channel opens
- [ ] Verify the official eligibility for an API-based visualization
- [ ] Complete any required identity or attribution proof
- [ ] Submit via official channel
- [ ] Obtain badge acceptance visible on Genesis account

## Safety and integrity

No requests for wallet signatures or gas fees are part of SQUEEKFOREST. Anyone asking for a seed phrase, private key, or payment to verify this read-only demo should be treated as suspicious. Badges, Aura and whitelist status are solely determined by the official Genesis platform.
