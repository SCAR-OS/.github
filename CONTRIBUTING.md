# Contributing to SCAR OS

## Where things live

- **Research, specs, architecture, milestones** → [`scar-os-docs`](https://github.com/SCAR-OS/scar-os-docs)
- **Code, build tooling, CI** → [`SCAR-OS`](https://github.com/SCAR-OS/SCAR-OS)

## Workflow

We work through open GitHub Issues in `SCAR-OS/SCAR-OS`. The module split
in the original proposal is a planning reference, not a restriction —
anyone can pick up any open issue:

1. Browse open issues, pick one that interests you, assign yourself.
2. Create a branch: `feat/<short-description>` or `fix/<short-description>`.
3. Implement, test, and run `make check` locally.
4. Open a PR referencing the issue (`Closes #N`).
5. Get it reviewed by someone **other than yourself** — self-approval isn't
   accepted, and review isn't restricted to a particular module.
6. After approval and passing checks, merge. Update `scar-os-docs/MILESTONES.md`
   only once the change is actually verified.

## Setting up

See `SCAR-OS/docs/setup/windows-wsl2.md` or `docs/setup/linux.md`, then:

```bash
bash scripts/bootstrap.sh
make check
```

## Security-sensitive changes

Anything touching policy, task execution, or `native/src/landlock` needs
an explicit look at `SCAR-OS/.claude/rules/security.md` — see `SECURITY.md`
in this repo for how to report a concern.
