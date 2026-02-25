# Purely Go

A home for Go projects that are designed to run *anywhere* without depending on the host.

The goal is simple: if you give the program its inputs (files + env vars), it should not need anything else "installed on the machine" to do its job.

## The rule

Projects here may rely on:

- ✅ Environment variables  
- ✅ The Go toolchain / standard library   
- ✅ Other Go modules
- ✅ Files we explicitly provide (workspace, config, inputs)

Projects here should **not** rely on:

- ❌ Shelling out to host binaries (`sh`, `bash`, `git`, `tar`, `make`, …)
- ❌ CGO
- ❌ External daemons (Docker/Podman, background agents, system services)
- ❌ Implicit host state (global config, magic paths, "works on my machine" tooling)

If it wouldn't work in a minimal container or a locked-down CI runner with only env vars + provided files, it probably doesn't belong here.

## Why

- **Portability:** same behavior across laptops, CI, containers, and restricted environments  
- **Reproducibility:** fewer hidden inputs, fewer surprises  
- **Security:** smaller surface area and less ambient authority  
- **Embeddability:** libraries first; CLIs are just one interface  

## What you'll find here

- Library-first Go tooling with clean, testable interfaces
- Deterministic behavior and explicit inputs/outputs
- Opinionated constraints that keep dependencies honest

## Projects

- **GoNativeBuildpacks** — Go-native, CNB-inspired source-to-image engine (library-first; no daemon; no shell-outs)

More coming soon.

## Contributing

- Prefer pure-Go dependencies
- Keep integrations optional and behind narrow interfaces
- Document inputs (env vars, files, flags) and outputs (files, logs, artifacts)

---

<p align="center">
  <img alt="purely-go snowglobe gopher" src="snowglobe.png" width="256" />
</p>

<p align="center">
  <sub>The Go Gopher is an original creation by <a href="https://reneefrench.blogspot.com/">Renée French</a>, licensed under <a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a>.</sub>
</p>