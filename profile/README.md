# SCAR OS

An AI-centred, developer-focused operating environment built on Fedora
Atomic/Silverblue — a final-year project (FYP 23F-02, Institute of Emerging
Technologies, Sukkur IBA University Khairpur Campus).

## The problem

Developers switch constantly between natural language intent ("find the
function that handles login", "run the tests for this module") and the
literal commands needed to act on it. SCAR OS adds a semantic interaction
layer on top of a standard Linux desktop — speech or text in English, Urdu,
or a mix — that proposes concrete operations on real files and projects,
under rules the AI cannot change, with every change authorized, recorded,
and reversible where possible.

## Intent Engine

The core research contribution: turning speech/text into a structured,
untrusted `CandidateOperation` (via whisper.cpp + a local LLM, grammar-
constrained to a fixed JSON schema) that only a deterministic Policy Engine
can authorize. The AI never executes anything directly — see
[`scar-os-docs/architecture`](https://github.com/SCAR-OS/scar-os-docs/tree/main/architecture)
for the full design.

## Repositories

| Repo | Purpose |
|---|---|
| [`SCAR-OS`](https://github.com/SCAR-OS/SCAR-OS) | Implementation: source code, build tooling, CI, developer docs |
| [`scar-os-docs`](https://github.com/SCAR-OS/scar-os-docs) | Research, specifications, architecture, milestones — the project's source of truth for *what* and *why* |

## Where we are

Early scaffolding stage: the dev environment, shared contracts, and build
tooling exist; the four subsystems (Intent, Semantic, Policy, Tasks) are
specified in `scar-os-docs` but not yet implemented. `scar-os-docs/MILESTONES.md`
tracks actual, verified progress — not plans.

## How development is organized

Work happens through GitHub Issues in `SCAR-OS/SCAR-OS`, open for any team
member to pick up — the module split in the original proposal is a
planning reference, not fixed ownership. Research and specification happen
in `scar-os-docs`; implementation and testing happen in `SCAR-OS`, linked
back to the issue and spec that motivated it.
