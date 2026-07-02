# ZilMate Docs

Source for the official **ZilMate** documentation, published with [Mintlify](https://mintlify.com) at [zilmate.mintlify.app](https://zilmate.mintlify.app).

ZilMate is a production-grade multi-agent AI runtime for Node.js and TypeScript. It ships a `zilmate` CLI, a `zilmate/server` SDK, a decentralized swarm of 30+ specialist agents organized as a Digital Corporation, long-term memory, background job scheduling with Upstash QStash, real-time voice via Deepgram, and — as of v1.10.4 — the **ZilMate Ubiquity** global-hotkey background service.

Product code lives at [`zero-sugar0/zilmate`](https://github.com/zero-sugar0/zilmate). This repo only contains the docs site.

## What's in here

```
.
├── docs.json                   # Mintlify config: theme, nav, tabs
├── introduction.mdx            # Landing page
├── quickstart.mdx              # Install + first request
├── configuration.mdx           # Env vars and setup
├── sdk/                        # createZilMate(), manager/coding/subagents, model selection
├── swarm/                      # Digital Corporation, departments, war rooms, safety firewall
├── memory/                     # Long-term memory, Corporate Wiki, session continuity
├── jobs/                       # Background jobs, scheduling, QStash webhooks
├── tools/                      # DevOps, SysOps, cloud storage, multimedia, browser/Composio
├── voice/                      # Real-time voice + chat integrations
├── ubiquity/                   # System-wide hotkey background service (v1.10.4)
├── cli/                        # zilmate CLI reference
└── changelog/                  # Product changelog
```

## Local preview

Install the Mintlify CLI once:

```bash
npm i -g mint
```

Run the dev server from the repo root (where `docs.json` lives):

```bash
mint dev
```

Open http://localhost:3000. Validate before pushing:

```bash
mint validate
mint broken-links
```

## Editing conventions

- All pages are MDX with YAML frontmatter (`title`, `sidebarTitle`, `description`).
- Sentence case for headings ("Getting started", not "Getting Started").
- Second-person voice, active tense.
- Internal links use root-relative paths (`/sdk/overview`), never full URLs.
- Register new pages under the correct group in `docs.json`.
- Code blocks always carry a language tag.

## Deployment

Merges to `main` trigger a Mintlify deploy automatically. Preview builds are attached to each PR. The site is live at [zilmate.mintlify.app](https://zilmate.mintlify.app).

## Reporting issues

- **Docs bugs, typos, missing content:** open an issue or PR against this repo.
- **Product bugs or feature requests:** file them at [zero-sugar0/zilmate](https://github.com/zero-sugar0/zilmate/issues).

## License

Documentation content follows the license in [`LICENSE`](./LICENSE). The ZilMate product is licensed separately in its own repo.
