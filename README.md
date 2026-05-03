# Nine Seconds — PocketOS Timeline

An interactive slow-motion replay of the April 24, 2026 PocketOS incident, when an AI coding agent deleted a SaaS company's production database in nine seconds.

**▶️ [View the live demo](https://mhsu2112.github.io/pocketos-nine-seconds/)**

## What this shows

The widget replays the full 9-second sequence in slow motion, showing what each layer of the supply chain was doing in parallel:

- **PocketOS** — the user and operator of the agent
- **Cursor** — the AI agent interface and harness
- **Claude Opus 4.6** — the LLM powering the agent
- **Railway** — the infrastructure hosting the database

Each event shows a plain-language description, the technical detail, and where applicable a "control flag" calling out what existed but didn't fire. Toggle to 1× at the end to feel the actual pace of the destruction — about as long as a single human breath.

## Source materials

The timeline is built from publicly available primary sources: the founder's X post, Railway's CEO's X posts and emailed statements to The Register, Railway's "Your AI wants to nuke your database" technical write-up, and reporting in The Register, NeuralTrust, Unite.AI, and Saviynt.

A companion NTSB-style post-mortem, an executive briefing, a TPRM supplemental examiner aid, and an autonomy-tiering justification memo (each in revised v2 form) are available separately and not included in this repo.

## Technical notes

- Single self-contained HTML file. No build step, no dependencies, no external scripts.
- Opens directly in any modern browser.
- Light and dark modes follow the system preference.
- Renders cleanly on desktop; usable on tablets; small phones may want landscape orientation for the timeline visualization.

## Caveats

The Claude (LLM) layer is described in deliberately conservative terms. Without the prompt stack, the harness tool policy, the session approval mode, the shell-execution trace, and the model-tool-call interface, public sources cannot resolve where in the agent system the destructive plan originated — model planning, harness tool affordances, session approval configuration, or some combination. The timeline reflects this rather than asserting a settled finding about the model's reasoning.

## License

MIT
