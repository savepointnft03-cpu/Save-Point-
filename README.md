# SAVE POINT — NFT Collection Website

Multi-page static website ready for GitHub Pages or any static host.

## Pages
- `index.html` — landing page and featured previews
- `collection.html` — 15 artwork concept previews, filtering, search and detail modal
- `mint.html` — wallet connect and transparent pre-launch mint status
- `archive.html` — collection concept and visual archive
- `about.html` — project information and FAQ

## Official X account
- `https://x.com/SavePointNFT` — linked from every page navigation and footer, plus a dedicated homepage follow section.
- Edit the URL and handle in each HTML file if the account changes.

## Run locally
Serve with a local HTTP server (fetch for `assets/nfts.json` may not work with file://):

```sh
python -m http.server 8000
```

Open http://localhost:8000. For GitHub Pages upload all files at repository root and enable Pages from the main branch/root.

## Important: pre-launch state
- 15 concept previews are cropped from the previously approved visual sheet. These are **not** 3,333 generated NFT images or deployed tokens.
- Wallet connection uses `window.ethereum` and `eth_requestAccounts`. No private keys, signatures, approvals or transactions are requested.
- Minting is intentionally disabled until contract address, correct Robinhood Chain network settings, deployed/verified ERC-721 contract, metadata hosting, and mint integration are ready.
- Mint price 0 ETH + gas, cap 3 per wallet, supply 3,333 are design specifications, **not yet enforced on-chain**.
- For best performance use WebP images and a static CDN (already optimized).
- Fonts are loaded from Google Fonts; fallbacks work offline.

## Next engineering milestones
1. Produce and quality-check all 3,333 unique images and deterministic metadata with trait constraints.
2. Decide storage (e.g. IPFS), provenance and reveal approach.
3. Deploy and test audited ERC-721 contract on target network testnet, with total supply and 3/wallet limit enforced.
4. Integrate transaction calls, chain switching and gas estimates using verified chain ID/RPC and contract ABI.
5. Test mobile wallets, errors, and launch readiness.


## Expanded concept gallery
The Collection page now shows 150 individually numbered derivative artwork previews. They are design studies built from the original 15 preview images, with different archive IDs, color accents, labels, stamps, and rarity tags. They are not the final 3,333 minted NFT artworks, nor are these token rarity distributions finalized.
