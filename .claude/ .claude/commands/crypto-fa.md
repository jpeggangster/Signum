# Crypto Fundamental Analysis

Perform a structured fundamental analysis on the cryptocurrency: **$ARGUMENTS**

Use WebSearch to research each pillar below. Run multiple searches in parallel where possible. Be specific — search for "$ARGUMENTS tokenomics unlock 2026", "$ARGUMENTS on-chain metrics TVL 2026", "$ARGUMENTS whale activity 2026", etc.

---

## Pillar 1 — Team & Backing
- Are the founders doxxed and credible?
- Who are the investors/VCs? Are they reputable?
- Any rug history or red flags?

## Pillar 2 — Technology & Roadmap
- What problem does it solve? Is there real demand?
- How does it compare to competitors?
- Is the roadmap being executed on time?

## Pillar 3 — Market Position & Narrative
- Is this narrative fading or growing (e.g. AI, DePIN, L2, privacy)?
- Is adoption growing or declining?
- Are major partnerships real or vaporware?

## Pillar 4 — Tokenomics & Unlocks (CRITICAL for short thesis)
- What is the total supply vs circulating supply?
- Are there upcoming token unlocks for team/investors? When and how large?
- Is inflation high? Is there a burn mechanism?
- Are vesting schedules creating persistent sell pressure?

## Pillar 5 — On-Chain Activity (CRITICAL for short thesis)
- Is TVL growing or declining?
- Are daily active users/transactions trending up or down?
- Is developer activity (GitHub commits) active or dead?
- Are protocol revenues increasing or collapsing?

## Pillar 6 — Exchange & Liquidity Health
- Is the token being delisted from major exchanges?
- Is liquidity thin or deep?
- Any regulatory actions targeting this asset?

## Pillar 7 — Whale & Institutional Sentiment (CRITICAL for short thesis)
- Are large wallets accumulating or distributing?
- Are institutions exiting positions?
- Is the number of holders growing or shrinking?

---

## Output Format

After researching, output EXACTLY this structure:

```
CRYPTO FA — [ASSET NAME] ([TICKER])

Pillar 4 (Tokenomics): [1-2 sentences on unlock risk / inflation]
Pillar 5 (On-Chain):   [1-2 sentences on activity trend]
Pillar 7 (Whales):     [1-2 sentences on large holder behaviour]

Other notes: [Any critical factor from pillars 1-3, 6]

OVERALL FA TIER: [Tier 1 / Tier 2 / Tier 3 / Tier 4]

Tier definitions:
  Tier 1 = Strong fundamentals (growing adoption, good tokenomics, institutional interest) — DO NOT SHORT
  Tier 2 = Decent fundamentals (mixed signals, some concerns) — AVOID SHORTING
  Tier 3 = Weak fundamentals (declining metrics, tokenomics headwinds, fading narrative) — SHORT CONFIRMED
  Tier 4 = Very weak fundamentals (collapsing usage, massive unlocks, regulatory action) — HIGH CONVICTION SHORT

FILTER 2 RESULT: PASS (Tier 3 or 4) / FAIL (Tier 1 or 2)
```
