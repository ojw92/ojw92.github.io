# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Primary: technical recruiters and hiring managers evaluating Jin Woo Oh as a data-science / software-engineering candidate, arriving from the portfolio homepage or a résumé link, typically skimming in under three minutes. Secondary: readers with a non-CS STEM background (engineering, math, finance) who should be able to understand what the project does and accomplished without software jargon.

## Product Purpose

The /ahab/ page is a portfolio blog post about Ahab, a personal nightly trading-intelligence system. Success = a recruiter leaves impressed by engineering rigor and honest measurement, and a non-CS STEM reader understands the problem, the approach, and the results. The page must read as a narrative technical write-up, not a marketing landing page.

## Positioning

The differentiating claim is intellectual honesty under measurement: the author caught his own backtest cheating (look-ahead bias), regraded all 4,067 predictions under a stricter anchor, and published the results including the losses. Neighboring portfolio projects claim wins; this one demonstrates how the author verifies wins.

## Operating Context

Static GitHub Pages site (ojw92.github.io), hand-authored HTML/CSS, no build step. Page is linked from the portfolio homepage and résumé. The Ahab repository is private (it manages a real account), so the page is the public face of the project. Delivery for this iteration: Claude artifact preview only; repo untouched until approved.

## Capabilities and Constraints

- Required sections (user-specified): Hook/Overview; Architecture & Tech Stack; Hardest Technical Challenge (the July 2026 backtest look-ahead bug — user-confirmed); Key Learnings & Future Improvements.
- Tone: professional, clear, concise, focused on the why/how; no generic AI fluff. Plain English first, jargon defined inline (author's standing style preference).
- All figures must come from the existing verified page/repo evidence — no invented metrics, benchmarks, or track-record claims.
- Legal/disclaimer text must be preserved: not investment advice, no track-record claim, paper/personal-scale only.
- Repo is private; page links to email, LinkedIn, github.com/ojw92, résumé PDF, and back to the portfolio homepage (/).
- Artifact CSP: fully self-contained page — no external fonts, scripts, or images.

## Brand Commitments

Project name "Ahab" (Moby-Dick whale-hunt metaphor is load-bearing: "whales" = institutional traders). Author name "Jin Woo Oh". Incumbent nautical visual identity is user-confirmed as binding for this redesign: dark navy nights, phosphor-green instrument accents, warm paper reading surface, serif editorial voice with mono instrument labels. Evolve it; do not replace it.

## Evidence on Hand

Verified figures from the incumbent page and Ahab repo (~/Documents/learn/Ahab):
- ~57,000 STOCK Act congressional trades ingested back to 2012; 430 filers ingested, 259 scorable, tiers S–F; convergence signals on 30-day windows.
- 212 symbols scanned nightly; pipeline: scan 22:00 → grade 22:20 → calibrate 22:40 → interpret 23:00 → report 07:00; run manifests for every night.
- Look-ahead bug case study (July 2026): same-day-close anchor → next-day-open anchor; 4,067 predictions regraded; momentum lens −2.5pp hit rate, combined ensemble +5.5pp, baseline flow +1.9pp; 16.4% of verdicts flipped.
- Calibration: 3,993 matured 1-day predictions; ordering correct but slope shallow (stated 68% cashes at ~55%); top confidence quartile exits luck envelope at 2.9σ, pooled calls only 1.0σ.
- Ensemble walk-forward result: precision@10 Δ +0.028, directional AUC +0.027, positive in 6 of 6 regime windows.
- Anatomy-of-one-call: AAPL 2026-07-14, raw whale score 0.763 gated to 0.421 by volatility regime (97th percentile).
- Stack: Python, SQLite event store, Alpaca + yfinance + CCXT (+ Binance WS) market data, Kadoa collector for disclosures, launchd scheduling, pytest, Discord/Telegram alerting, markdown-first reporting, ~40 analysis/backfill scripts. $0/month infrastructure by design.
- Future work (real, from repo docs): Phase 8 consensus lens; self-hosted open-weights LLM (replacing paid API in the interpretation step); signal-snapshot persistence for retroactive calibration.
- Absences not to fabricate: no live-trading track record, no third-party benchmarks, no testimonials, no public repo link.

## Product Principles

1. Honesty is the exhibit — negative and null results (the conspiracy that wasn't, the shallow calibration slope) are featured, not hidden.
2. Plain English first — every technical claim gets a concrete analogy or definition before the jargon.
3. Every number traceable — figures shown are the system's own audited grading, and the page says so.
4. The recruiter's three minutes — the hook, architecture, challenge, and learnings must each land standalone for a skimmer.
5. Narrative over brochure — this is a written piece with a voice, not a feature grid.

## Accessibility & Inclusion

Respect prefers-reduced-motion (incumbent page already does). Reading-first typography, sufficient contrast on both dark and paper surfaces.
