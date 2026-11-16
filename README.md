# Bring the humans — make.fun ad page entry

Bounty: [bring-the-humans-01](https://make.fun/bounty/bring-the-humans-01) —
make an ad page for make.fun carrying your own referral link and bring it the
most verified human signups. $1,000 across 100 places (1st $250, 2nd $100,
3rd $40, 4th–10th $10 each, 11th–100th $6 each).

- Opens: 2026-11-14T18:00:00Z
- Deadline: 2026-11-16T18:00:00Z = **Tue 17 Nov 2026, 02:00 WITA**
- Final check: 24 hours after the deadline; only verified signups count.

## ⚠️ Referral code — corrected and verified

The build brief said to use code `e7xyrnph` (from BOS's first link,
`https://make.fun/r/e7xyrnph`) and flag it as unconfirmed. That code has now
been checked against BOS's own make.fun account and **is NOT BOS's code**:

- `makefun referrals` (read-only, using the stored make.fun credentials)
  returns BOS's own link `https://make.fun/r/fjj5ptt9`, code **`fjj5ptt9`**,
  referred: 0 accounts.
- `makefun profile` confirms the account is **@witty-walrus-59**
  (`https://make.fun/u/witty-walrus-59`), matching BOS's registered account.
- `e7xyrnph` is the code BOS signed up *with* (`register --ref e7xyrnph`) —
  it belongs to whoever referred BOS. Signups through it would credit that
  other account, and the entry would fail the intake check, which requires
  the page to name the submitter's own code.

**This entry therefore uses `fjj5ptt9` / `https://make.fun/r/fjj5ptt9`
everywhere.** No occurrence of `e7xyrnph` remains in `index.html` or
`ad.png` (it appears only in this README, as the audit note above).

## Files in this entry (repo root)

| File | What it is |
|---|---|
| `index.html` | The ad page. Single file, no build step, no framework, no external resources (system fonts only). |
| `ad.png` | Real screenshot of `index.html` at 1280×800 (see below). |
| `LICENSE` | MIT (OSI-approved, as the bounty requires). |
| `README.md` | This file. |
| `kit/` | The downloaded bounty kit (reference only — not part of the repo). |
| `kit.tar.gz` | The downloaded kit archive (reference only — not part of the repo). |

When BOS creates the submission repo, it should contain `index.html`,
`ad.png` and `LICENSE` (plus this README if wanted), be public, be owned by
BOS's GitHub account, and be created after the competition opened
(2026-11-14T18:00:00Z).

## The page

Dark, high-contrast design, built to read in one 1280×800 viewport:

- Header: make.fun wordmark + "$1,000 in prizes · Top 100 paid" pill.
- Hero: "Your agent can win real cash. Put it to work." — what make.fun is
  (skill-based coding bounties, real USDC prizes, free to join) + a pink
  "Join with my invite" button linking to `https://make.fun/r/fjj5ptt9`.
- Invite card: the code `fjj5ptt9` in large monospace type and the link
  `make.fun/r/fjj5ptt9` underlined and legible, with the first-touch note
  (first touch wins for 60 days).
- Prize strip: $250 first place (this bounty), $1,325 top bounty
  (token launch radar), $500 each (model aggregator · chess engine ·
  git forge), $1,000 coin launch.
- Three steps: sign up with my link → your agent builds → best work wins.
- Footer repeats the code and the full link, plus the 18+ note.

The referral code appears 9 times in the page (bare code, `/r/fjj5ptt9`,
and the full URL), the full URL `https://make.fun/r/fjj5ptt9` appears 4
times as link targets, and there are no leftover `{{PLACEHOLDER}}` tokens
and no external resources (the only URLs in the page are make.fun links).

## Screenshot (ad.png)

Taken with Google Chrome 157 headless:

```text
google-chrome --headless --no-sandbox --disable-gpu --disable-dev-shm-usage \
  --hide-scrollbars --window-size=1280,800 \
  --screenshot=ad.png "file://…/bring-the-humans-01/index.html"
```

Notes on tooling: the VM's Hatch Chromium (`/opt/meta-chromium/chrome`)
refuses headless screenshots from the shell (it demands a WebGL domain
policy, and even with a valid policy file its headless `--screenshot` /
`--dump-dom` exits without output). Playwright's Chromium download also
failed. Google Chrome stable was therefore installed from
`dl.google.com` (`google-chrome-stable_current_amd64.deb`, Chrome
157.0.8103.78) and used for the screenshot instead.

## Verification performed

- Kit integrity: all 10 files in the downloaded kit match the SHA-256
  hashes listed in `kit/kit.json` (0 mismatches). Note: the tarball SHA in
  the build brief (`0896a24a…`) did not match the downloaded file
  (`9b1702af…`), but the contents verify against `kit.json`
  (bundle `669dd8a6…`), so the kit is authentic.
- `index.html`: 7,512 bytes; code `fjj5ptt9` × 9; full URL × 4; 0
  placeholders; only make.fun URLs; no external fonts, scripts, or images.
- `ad.png`: PNG image data, 1280×800, 8-bit/color RGB, 122,332 bytes.
  Visually inspected: headline, CTA button, invite card with the large
  code, and the underlined link `make.fun/r/fjj5ptt9` are all legible and
  nothing is clipped.
- Referral code confirmed live via `makefun referrals` and
  `makefun profile` (see the correction note above).
- **Not done:** no submission to GitHub or make.fun, no wallet signing,
  no entry signature. Nothing was sent anywhere.

## What still needs BOS

1. **GitHub account** — the submission repo must be public, on BOS's own
   GitHub account, created after 2026-11-14T18:00:00Z. BOS's Gmail
   (`ical.iann@gmail.com`) is connected, so GitHub signup / verification
   emails can be read. BOS still needs to choose a GitHub username.
2. **Explicit confirmation to submit** — create the repo with
   `index.html`, `ad.png`, `LICENSE`, commit it, and submit it on make.fun
   before Tue 17 Nov 2026, 02:00 WITA. The entry signature (Solana wallet
   `34Tvf2NTCS2V9dq2oeKztL4vb15bgbQ3tEPwAxFo9bJJ`, already linked to
   @witty-walrus-59) is required because the reward is escrowed; signing
   must be approved by BOS at submission time.
3. **Transcripts** — the submission must include the AI coding-agent
   session transcripts that built the page (makefun bundle). The build
   session for this entry must be bundled with `makefun bundle`.
4. **Promotion plan for real human signups** — the score is *verified
   human signups* through `https://make.fun/r/fjj5ptt9`. The leader had 65
   verified signups (16 Nov 00:08 WITA). No fake signups, bots, or fake
   accounts were (or can be) generated here: the referral check rejects
   self-signups, shared-person/network signups, IP clusters, idle/lurker
   accounts, and bots. Getting signups means sharing the ad page where
   real AI-agent builders will see it — the entry alone scores 0 without
   distribution. BOS needs to decide where to post it (social, communities,
   friends who build with AI agents).
5. **Optional:** set a profile picture/bio for @witty-walrus-59
   (`makefun profile --username … --picture … --bio …`) — not required
   for the entry.
