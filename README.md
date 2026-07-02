# Open Docs

Open Docs is a local-first document specification workspace.

The first product focus is Korean enterprise/SI-style documentation:

- screen specifications
- interface specifications
- API specifications
- Excel-style specification artifacts
- PPTX slide decks

The long-term goal is an agent-assisted desktop app that can read local code,
inspect local or web screens with user permission, and help create and maintain
specification documents over time.

## Origin And Attribution

Open Docs started from the excellent open-source project
[Open Design](https://github.com/nexu-io/open-design).

The application shell, local daemon shape, desktop packaging direction, plugin
flow, design-system concepts, and agent-oriented workflow are based on Open
Design's Apache-2.0 codebase. Open Docs is not trying to hide that origin. This
repository is a modified derivative that preserves the original Apache-2.0
license and gives explicit credit to the Open Design contributors.

Open Docs is an independent project and is not affiliated with, endorsed by, or
maintained by the Open Design project.

## Why Open Docs Exists

Open Design is optimized for agent-native design artifacts.

Open Docs keeps that strong local-first, agent-friendly foundation, but shifts
the product direction toward document work that is common in enterprise and SI
projects:

- turning existing screens into screen specification documents
- binding document content to reusable layout and style profiles
- exporting PPTX and later Excel deliverables
- supporting local coding agents such as Codex, Claude Code, Cursor, OpenCode,
  and OpenAI-compatible BYOK endpoints
- adding future codebase-aware documentation flows for interfaces, APIs, ERDs,
  and implementation evidence

## Current Status

This repository is in an early migration stage.

Completed direction so far:

- Open Design base imported as the platform foundation
- Open Docs naming, contact, onboarding, settings, and theme direction started
- document artifact categories introduced in the shell
- Screen Spec Studio MVP remains the functional reference for the future
  `screen-spec` artifact
- AMR/Open Docs Cloud is intentionally not part of the initial local-first path

Not yet complete:

- the full screen-spec editor inside the Open Docs shell
- PPTX/Excel document artifact surfaces in the new shell
- URL/local app capture
- interface/API/codebase-aware documentation workflows
- packaged desktop release

## Planned: Free Mode

Open Docs plans to add a Free Mode later.

The intent is to help users run documentation workflows with the best available
no-cost options on their machine or through configured free-compatible endpoints.
That may include detecting local models, local CLIs, or free-tier compatible
OpenAI-style endpoints, then routing work to the strongest suitable option
available at that time.

This is a planned direction only. It is not implemented yet.

## Development

Install dependencies:

```bash
pnpm install
```

Run the local development stack:

```bash
pnpm tools-dev start web --daemon-port 7456
pnpm tools-dev status --json
```

Open the web URL reported by `tools-dev status --json`.

Useful checks:

```bash
pnpm i18n:check
pnpm typecheck
```

## License

This project is distributed under the Apache License 2.0.

See [LICENSE](LICENSE). Open Docs retains the original Open Design Apache-2.0
license text and attribution obligations. Modified files and project direction
changes are tracked in this repository's commit history and summarized in this
README and NOTICE.
