# Agents in the Large Publication Entry

## Goal

Add the paper “Agents in the Large: Perception-Centered Architecture for Persistent Agents” (arXiv:2608.30478) to the homepage’s Publications section and announce its release in News.

## Content Design

- Add a `2026.08` News item at the top of the News list announcing that **Agents in the Large** has been released on arXiv.
- Add a new publication card at the top of `L3-Agent`, matching the existing `paper-box` markup and using the `Arxiv 2026` badge.
- Preserve the arXiv author order, bold **Shichun Liu**, and mark the first three authors as equal contributors.
- Summarize the paper in two concise bullets:
  1. Motivate the transition from bounded, user-specified tasks to persistent assistance in long-lived settings.
  2. Explain how Pera combines active perception and lifecycle-level control to formulate lifecycle tasks and adapt the agent’s ongoing service.
- Link the Paper badge to `https://arxiv.org/abs/2608.30478`.
- Use the paper’s Figure 3—the conceptual Pera architecture—as the publication thumbnail, stored as `images/pera-main.png`.

## Scope and Verification

Only `_pages/about.md` and the new image asset are changed during implementation. Existing uncommitted edits in `_pages/about.md` are preserved. Verification will check the final diff, referenced asset, publication ordering, author metadata, link, and local site build if the repository’s current toolchain supports it.
