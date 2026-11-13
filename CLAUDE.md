# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

A trip-planning workspace for a January 2027 group ski trip to Whistler Blackcomb, not a code project. There is nothing to build, lint, or test; the work is research and keeping three Markdown files current.

- `TRIP-PLAN.md` — **single source of truth.** Goal, open questions, decisions log, participants, itinerary, logistics, budget, pricing worksheets (§7a-7c), session log. Read it first and update it every session.
- `Specifics.md` — the owner's original trip parameters (levels, dates, origin, lodging preferences, notes).
- `PROMPTS.md` — verbatim log of every user prompt.

## Standing rules

- **Log every user prompt verbatim in `PROMPTS.md` (numbered, newest last, above the trailing italic note) before acting on it.**
- **No participant names, and no GitHub username, in any file.** Refer to people as "the rider", "Skier 1", etc. Names and the username were deliberately redacted from the files and the git history; do not reintroduce them (including in PROMPTS.md quotes, where they are shown as `[Rider]`, `[Name removed]`).
- The trip goal in `TRIP-PLAN.md` §1 is locked: bonding plus enjoying the region. Measure choices against it.
- When facts change, update the decisions log and session log in `TRIP-PLAN.md`, not just the section that changed.
- Mark anything not verified live as unverified. Past searches only returned stale "from" prices; the pricing sections say so explicitly. Do not present estimates as quotes.

## Researching prices (what works and what doesn't)

- `WebSearch` returns undated or stale prices; use it for facts (passes, restricted dates, activities), not quotes.
- `WebFetch` on Airbnb search URLs (with `checkin`/`checkout`/`adults`/`min_bedrooms` and map bounds) returns usable live listings; results are summarized and truncated, so give each listing's `/rooms/ID` link and tell the owner to verify.
- Vrbo, Expedia (429), Booking.com and Whistler.com (403/empty), Google Flights and Kayak (no data) have not worked. Flights and hotels still need quotes from the owner running the searches in a browser.

## Git

- Remote: private GitHub repo `origin` (`main`). History was squashed once to remove names; it is a normal linear history now.
- Commit author must use the GitHub noreply email already set in this repo's local git config, or pushes are rejected (GH007 private-email protection). Do not change global git config.
- Commit and push `PROMPTS.md` and `TRIP-PLAN.md` after changes; commit messages end with the attribution line given in the session instructions.
