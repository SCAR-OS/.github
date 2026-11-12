# Security policy

SCAR OS is a final-year project in active early development; nothing here
runs in production yet. That said, the Policy & Security Engine design is
a core part of the project, so we still want to know about real issues.

## Reporting

Open a private report via GitHub's "Report a vulnerability" on
[`SCAR-OS/SCAR-OS`](https://github.com/SCAR-OS/SCAR-OS/security/advisories/new),
or contact a maintainer directly rather than filing a public issue if the
concern involves a real exploit path.

## Scope

Relevant now: anything that would let an LLM-generated `CandidateOperation`
bypass the Policy Engine, or defeat the intended Private Space isolation
once implemented. See `SCAR-OS/docs/security/security-invariants.md` for
the invariants we're building against — a report that shows one of them
can be violated is in scope even before the corresponding subsystem is
fully implemented.
