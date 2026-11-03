# GLofter development plan

**Owner:** wang checks boxes when a task is done on `main` (or demo evidence exists). Hiker answers questions only.

**How to use:** Change `- [ ]` → `- [x]` and date the **Status** line when you complete an item. Do not check partial work unless acceptance criteria are met.

**Status:** Plan published 2026-11-03. P0.1–P0.2 + P0.3 + P0.4 + P0.6 done.

---

## Done (pre-checked)

- [x] Org repos + app first push; box gh HTTPS push
- [x] `studio#1` thumb/EXIF backfill on `main`
- [x] Official site Pages + `glofter.com` / `www` custom domain
- [x] Phase0–5 baseline: Choice B, media upload, DID Connect island, signed Hub join, theme packs

---

## P0 — honesty / demo (~5–7 person-days)

- [x] **1.** Sync `glofter-arc` monorepo ← `studio#1` — **0.5d**
- [x] **2.** Demo DB run `backfill:photo-thumbs` (dry-run → apply) + record result — **0.5d**
- [x] **3.** Fix themes ZIP download 503 — **1d**
- [x] **4.** `protocol` Photo + `thumbUrl` DTO + Studio/Hub docs — **0.5d**
- [ ] **5.** OSS cleanup: secrets/local paths/private notes, LICENSE, honest READMEs — **2d**
- [x] **6.** Org development plan page live + checkbox workflow — **0.5d** (Hiker writes, wang maintains checks)

---

## P1 — product loop (~10–14d)

- [ ] **7.** TransferV2 auto encode/broadcast into booking-pay (flag-gated, no PaymentKit) — **3–4d**
- [ ] **8.** AUP in-daemon real SPA (or document shell-only) — **3–4d**
- [ ] **9.** Studio joined-hubs table + manage list — **1–2d**
- [ ] **10.** Hub binary image sync (or label JSON-cards-only) — **2–3d**
- [ ] **11.** App store prep: `eas init` projectId, credentials, store materials — **2d** (needs user accounts)

---

## P2 — later (~8–12d)

- [ ] **12.** Media GIF/HEIC policy + full resize + orphan cleanup — **3–4d**
- [ ] **13.** Object storage/CDN adapter — **3–4d**
- [ ] **14.** On-chain/NFT resolve signed-join pubkey — **2–3d**
- [ ] **15.** Signed Studio→Hub content push — **2–3d**

---

## Frozen (do not schedule)

PaymentKit / Stripe / SubGuard / mainnet real money; CNY→TBA FX; paid theme market; legacy React theme runtime.

---

## Milestones

| ID | Definition | Calendar (Asia/Shanghai, ~1 FTE wang) |
|----|------------|----------------------------------------|
| **M1** | Open-source demo = all **P0** | ~1.5 weeks |
| **M2** | Beta loop = **P1** items **7–10** | +~3 weeks (~**5 weeks** cumulative) |
| **M3** | App submit-ready = **P1 #11** (parallel) | Blocked on user accounts |
| **M4** | Enhancements = **P2** after M2 | After M2 |

### Totals

- **M1:** 1–1.5 weeks  
- **M1 + M2:** ~4–5 weeks  
- **With App prep:** ~5–6 weeks  
- **Full P2:** ~7–9 weeks  

**Risks:** AUP in-daemon vs shell-only; TransferV2 encode/broadcast into booking-pay.

---

## Progress log

| Date | Milestone | Note |
|------|-----------|------|
| 2026-11-03 | Plan | Plan published; `studio#1` done; site on Pages |
| 2026-11-03 | P0.6 | Plan page live on glofter/.github DEVELOPMENT_PLAN.md |
| 2026-11-03 | P0.1 | Synced glofter-arc ← studio#1 (media-backfill + tests); node test pass |
| 2026-11-03 | P0.2 | Demo backfill: dry-run 1 raster + 7 svg skip; apply processed=1 (pho_5a5c51e05279389d); record in glofter-arc docs/backfill-demo-2026-11-03.json |
| 2026-11-03 | P0.3 | studio#2 + hub#1 on main: vendored theme ZIP (no themes package); themes download 503 fixed |
| 2026-11-03 | P0.4 | protocol#1 Photo.thumbUrl + studio#3 honesty docs |
