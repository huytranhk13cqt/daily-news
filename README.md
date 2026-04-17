# daily-news

An automated daily digest of the Data Engineering and IoT ecosystems, produced every morning at 07:00 AWST by a scheduled Claude Code agent and committed directly to this repository.

## What lives here

Each day produces one markdown file under `news/YYYY/MM/YYYY-MM-DD.md` containing four to six curated items across Data Engineering and IoT. Every item follows a fixed schema (title, metadata table, Overview → Details → Takeaway content flow, example snippet, sources) so the files are both readable by a human skimming them over coffee and parseable by tooling for later search and visualisation.

## How it works

A Claude Code scheduled routine fires once per day at 23:00 UTC (which is 07:00 the following calendar day in Perth, Western Australia). On each run the agent clones this repo, scans a rotating subset of around fifteen engineering blogs, release feeds, and GitHub release pages across the two domains, selects the items that pass a three-part gate (recent, substantive, non-duplicate), writes the digest file according to the schema, then commits and pushes.

## Key files

The schema every digest file must follow is defined in [`TEMPLATE.md`](./TEMPLATE.md). The reasoning behind the source pool, selection criteria, and design choices is documented in [`METHODOLOGY.md`](./METHODOLOGY.md). A hand-crafted example showing what a finished digest looks like lives at `news/2026/04/2026-04-18.md` (this file is an illustrative example, not a real digest).

## Maintainer notes

This repository is maintained by Coffee ([huytranhk13cqt](https://github.com/huytranhk13cqt)) as part of a broader personal knowledge infrastructure for a Data Engineer career track targeting the Perth, WA market. The system is intentionally minimal — one file per day, one commit per run, no database, no frontend — to keep operational overhead at zero while still producing durable historical coverage.

Feedback, source suggestions, and pull requests are welcome.
