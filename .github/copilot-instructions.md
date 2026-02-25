# Copilot Instructions for purely-go/.github

## Repository Overview

This is the **organization-wide `.github` repository** for the [`purely-go`](https://github.com/purely-go) GitHub organization. It contains:

- `README.md` — the organization profile displayed on the `purely-go` GitHub page
- `profile/` — assets used in the organization profile (e.g. `snowglobe.png`)
- `.github/` — repository settings and Copilot instructions (this directory)

There is no build system, no Go source code, and no test suite in this repository. Changes here are purely documentation, configuration, and profile assets.

## Organization Philosophy

The `purely-go` organization hosts Go projects that must run **anywhere** without depending on the host environment beyond env vars and explicitly provided files.

### Projects in this org MAY rely on

- Environment variables
- The Go toolchain / standard library
- Other Go modules (pure-Go dependencies preferred)
- Files explicitly provided as inputs (workspace, config, inputs)

### Projects in this org must NOT rely on

- Shelling out to host binaries (`sh`, `bash`, `git`, `tar`, `make`, …)
- CGO
- External daemons (Docker, Podman, background agents, system services)
- Implicit host state (global config, magic paths, ambient tooling)

## Making Changes

Since this repo contains no code, the only valid changes are:

1. **Documentation** — edit `README.md` to update the organization profile text or project list.
2. **Profile assets** — add or update images in `profile/`.
3. **GitHub configuration** — add or update files in `.github/` (e.g. issue templates, workflow files, Copilot instructions).

No build, lint, or test commands are needed. Simply edit the relevant Markdown or asset files.

## Key Files

| Path | Purpose |
|------|---------|
| `README.md` | Organization profile shown on github.com/purely-go |
| `profile/snowglobe.png` | Mascot image displayed in the README |
| `.github/copilot-instructions.md` | This file |

## Contribution Guidelines

- Keep language consistent with the existing README tone (clear, concise, opinionated).
- Prefer pure-Go dependencies in any referenced projects.
- Document inputs (env vars, files, flags) and outputs (files, logs, artifacts) in project descriptions.
- Do not introduce shell scripts, Makefiles, or host-binary dependencies in this repository.
