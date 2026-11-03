# GLofter

**Decentralized photography studios and discovery hub** — DID identity, portfolios, services, and booking. Migrating from ArcBlock Blocklet to the **ARC** stack.

Official site: [glofter.com](https://glofter.com)

## What it is

GLofter helps photographers run a branded studio on the open web while a Hub helps clients discover studios and book sessions. Identity and payments lean on ArcBlock DID (testnet TBA for payments while we harden UX and security).

Design goal: clean, portfolio-first UI — each photographer as a brand.

## Repositories

| Repo | Role |
|------|------|
| [studio](https://github.com/glofter/studio) | Photographer studio (site + manage / booking) |
| [hub](https://github.com/glofter/hub) | Multi-studio discovery & join network |
| [protocol](https://github.com/glofter/protocol) | Shared protocol & types |
| [themes](https://github.com/glofter/themes) | Theme packs (manifest + layouts) |
| [website](https://github.com/glofter/website) | Marketing / docs for glofter.com |
| [app](https://github.com/glofter/app) | Mobile client (Expo / React Native) |

Most repos are private while the ARC rebuild and usability testing finish; we plan to open-source when the public surface and honesty/security bar are solid.

## Stack (direction)

- **ARC** CLI / AUP hosting · Node ≥ 24 · pnpm 10
- Studio/Hub: Fastify + SQLite (booking backend kept through the rebuild)
- DID Connect for login; TransferV2 on TBA for booking payment experiments
- Themes as real packs, not CSS tokens only

## Status

Active rebuild under org `glofter`. Legacy monorepo lived at `shenxiuqiang/glofter`. Payment stays conservative (no mainnet real-money flows until photographer UI and security are solid).

## Contact

- Site: [glofter.com](https://glofter.com)
- Org: [github.com/glofter](https://github.com/glofter)
