# Project Claw Code

<p align="center">
  <strong>⭐ The fastest repo in history to surpass 50K stars, reaching the milestone in just 2 hours after publication ⭐</strong>
</p>

<p align="center">
  <a href="https://star-history.com/#ultraworkers/claw-code&Date">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=ultraworkers/claw-code&type=Date&theme=dark" />
      <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=ultraworkers/claw-code&type=Date" />
      <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=ultraworkers/claw-code&type=Date" width="600" />
    </picture>
  </a>
</p>

<p align="center">
  <img src="assets/sigrid-photo.png" alt="Claw Code" width="500" />
</p>

<p align="center">
  <strong>A community-built coding harness built on open agent frameworks</strong>
</p>

---

## Built With

This project is built and maintained using a combination of open agent frameworks:

- [**clawhip**](https://github.com/Yeachan-Heo/clawhip) — event-to-channel notification router and orchestration layer
- [**oh-my-openagent (OmO)**](https://github.com/code-yeongyu/oh-my-openagent) — open-source agent framework
- [**oh-my-codex (OmX)**](https://github.com/Yeachan-Heo/oh-my-codex) — Codex CLI extensions and workflow tools
- [**oh-my-claudecode (OmC)**](https://github.com/Yeachan-Heo/oh-my-claudecode) — Claude Code workflow extensions

> [!IMPORTANT]
> The active Rust workspace now lives in [`rust/`](./rust). Start with [`USAGE.md`](./USAGE.md) for build, auth, CLI, session, and parity-harness workflows, then use [`rust/README.md`](./rust/README.md) for crate-level details.

---

## Backstory

This project began as a community response to the Claude Code exposure, and has since grown into a serious engineering effort to build the most capable open coding harness possible.

The entire development is orchestrated using the open agent frameworks listed above, with parallel code review, persistent execution loops, and architect-level verification driven through agent workflows.

The project is actively maintained by a distributed team using open tooling — no proprietary infrastructure required.

See the full origin story and recent updates here:

https://x.com/realsigridjin/status/2039472968624185713

---

## Repository Layout

```text
.
├── src/                                # Python porting workspace
│   ├── __init__.py
│   ├── commands.py
│   ├── main.py
│   ├── models.py
│   ├── port_manifest.py
│   ├── query_engine.py
│   ├── task.py
│   └── tools.py
├── tests/                              # Python verification
├── assets/omx/                         # OmX workflow screenshots
├── 2026-03-09-is-legal-the-same-as-legitimate-ai-reimplementation-and-the-erosion-of-copyleft.md
└── README.md
```

## Python Workspace Overview

The new Python `src/` tree currently provides:

- **`port_manifest.py`** — summarizes the current Python workspace structure
- **`models.py`** — dataclasses for subsystems, modules, and backlog state
- **`commands.py`** — Python-side command port metadata
- **`tools.py`** — Python-side tool port metadata
- **`query_engine.py`** — renders a Python porting summary from the active workspace
- **`main.py`** — a CLI entrypoint for manifest and summary output

## Quickstart

Render the Python porting summary:

```bash
python3 -m src.main summary
```

Print the current Python workspace manifest:

```bash
python3 -m src.main manifest
```

List the current Python modules:

```bash
python3 -m src.main subsystems --limit 16
```

Run verification:

```bash
python3 -m unittest discover -s tests -v
```

Run the parity audit against the local ignored archive (when present):

```bash
python3 -m src.main parity-audit
```

Inspect mirrored command/tool inventories:

```bash
python3 -m src.main commands --limit 10
python3 -m src.main tools --limit 10
```

## Current Parity Checkpoint

The port now mirrors the archived root-entry file surface, top-level subsystem names, and command/tool inventories much more closely than before. However, it is **not yet** a full runtime-equivalent replacement for the original TypeScript system; the Python tree still contains fewer executable runtime slices than the archived source.


## Community

<p align="center">
  <a href="https://discord.gg/6ztZB9jvWq"><img src="https://img.shields.io/badge/Join%20Discord-6ztZB9jvWq-5865F2?logo=discord&style=for-the-badge" alt="Join Discord" /></a>
</p>

Join the [**claw-code Discord**](https://discord.gg/6ztZB9jvWq) — come chat about LLMs, harness engineering, agent workflows, and everything in between.

## Star History

See the chart at the top of this README.

## Ownership / Affiliation Disclaimer

- This repository does **not** claim ownership of the original Claude Code source material.
- This repository is **not affiliated with, endorsed by, or maintained by Anthropic**.
