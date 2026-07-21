# The Paranormal Archivist

> A utility-focused, data-driven paranormal investigation app for Android. The
> smartphone is treated as a sensitive environmental diagnostic instrument. The
> defining objective is **absolute immersion through a grounded, academic lens**.

**Platform:** Android (via Flutter / Dart)
**Aesthetic:** "Vintage Investigator" / Analog Horror — 1970s research society,
reel-to-reel tapes, distressed field journals, tactile brass/glass gauges.
**Data posture:** Offline-first and privacy-centric. All investigation data lives
on-device. From Phase 3 the user may *choose* to back it up to their **own** cloud
(Drive/OneDrive) and opt in to GPS site tagging — but there are no accounts, no
servers of ours, and **no telemetry, analytics, or ads, ever**. Nothing leaves the
device without an explicit user action. See
[`ADR-004`](docs/decisions/ADR-004-connectivity-and-cloud.md).

---

## Who does what

This is a **planning-led** project. Responsibilities are split cleanly:

| Role | Owner | Responsibility |
|------|-------|----------------|
| Project Manager / Architect | **Claude PM** (this workspace) | Specs, architecture, backlog, handoffs, review, documentation upkeep. **Writes no application code.** |
| Implementation | **Claude Code** | Executes handoff documents, writes/edits the Flutter code, reports back. |
| Product owner | **Nate** | Direction, priorities, approvals, final sign-off. |

The full working loop is defined in [`docs/PIPELINE.md`](docs/PIPELINE.md).

---

## Document map

```
Archivist/
├── README.md                         ← you are here
├── docs/
│   ├── PIPELINE.md                   ← how we work: plan → handoff → build → review
│   ├── ARCHITECTURE.md               ← modular architecture design document
│   ├── BACKLOG.md                    ← phased sprint backlog (MVP vs. expansion)
│   ├── TROUBLESHOOTING.md            ← environment/toolchain gotchas (not app bugs)
│   └── decisions/                    ← Architecture Decision Records (ADRs)
│       ├── ADR-001-tech-stack.md
│       ├── ADR-002-audio-engine.md
│       └── ADR-003-local-persistence.md
├── handoffs/
│   ├── _TEMPLATE.md                  ← blank handoff template for Claude Code
│   ├── HANDOFF-001-scaffold-and-emf.md
│   └── HANDOFF-002-journaling-and-followups.md
├── reviews/                          ← post-implementation review verdicts
│   ├── REVIEW-001.md
│   └── REVIEW-002.md
└── _to_delete/                       ← quarantine; Nate empties it (never delete directly)
```

## Current status

**Phase:** Phase 1 MVP in progress — Sprints 1 & 2 complete and reviewed (PASS).
**Built:** 3-tab shell, themed design-token system, sensor abstraction layer, live
EMF meter (100+ fps on device), Drift/SQLite journaling with Archives + save-session.
**Next action:** HANDOFF-003 — Audio EVP recorder (P1-E3).

See [`docs/BACKLOG.md`](docs/BACKLOG.md) for the full roadmap.
