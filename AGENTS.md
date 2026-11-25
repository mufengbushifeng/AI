# AGENTS.md

## Agent skills

### Issue tracker

Issues and specs are tracked as local Markdown files under `.scratch/`. See `docs/agents/issue-tracker.md`.

### Triage labels

The five default triage labels are used as-is. See `docs/agents/triage-labels.md`.

### Domain docs

Single-context layout: one root `GLOSSARY.md` plus `docs/adr/`. See `docs/agents/domain.md`.

## gstack

gstack v1.96.0.0 is installed globally from `~/gstack`. Its skills are available as user-level WorkBuddy skills named `gstack-*` (also registered under `~/.codex/skills`).

### Routing

- Start a new idea with `gstack-office-hours`; then use `gstack-plan-ceo-review`, `gstack-plan-eng-review`, `gstack-plan-design-review`, or `gstack-plan-devex-review` as appropriate.
- For existing code: `gstack-investigate` for root-cause debugging, `gstack-review` for changes since a baseline, `gstack-qa` for browser/API/CLI behavior, and `gstack-ship` for tests, review, and PR.
- Use `gstack-browse` for all web browsing and screenshots. Never use `mcp__claude-in-chrome__*` tools.
- `gstack-careful`, `gstack-guard`, `gstack-freeze`, and `gstack-unfreeze` are advisory on this host (no enforcing hooks).

### Working rules

- **Boil the Ocean** — complete coverage, minimal code: cover tests, edge cases, and error paths; write nothing beyond the requirement. Record any shortcut as an explicit decision.
- **Search before building** — know what exists before deciding what to build.
- **Reuse ladder** — repo helper → standard library → platform feature → installed dependency → new code. Fix root causes, not symptoms.
- **User sovereignty** — models recommend, the user decides. Ask before changing a stated direction.
- **Voice** — direct and concrete: name the file, function, command, and user-visible impact. No filler.

### Notes

- `gstack-cso` is unavailable until Visual Studio 2022 Build Tools with Desktop development with C++ are installed and `./setup --host codex --prefix` is rerun.
- Upgrade with `cd ~/gstack && ./setup --host codex --prefix`, or invoke the `gstack-upgrade` skill.

<!-- gbrain:brain-first:begin -->
<!-- gbrain brain-first v2: managed by gbrain and replaced on upgrade; edit outside these markers. Opt out: gbrain setup <harness> --instructions-only --no-instructions -->
## Memory: check GBrain first

GBrain (the `gbrain` MCP server) holds this user's notes, people, companies, meetings and decisions.

- Before answering any turn, check GBrain first, before files, mail or other sources: `recall` for what was said or decided, `entity` for a person or company.
- Fill gaps with your other tools. On an empty or thin result, retry with words the notes would use: synonyms, the formal name, the owner, several joined with OR.
- Brain results span every source the token can read, so apply your own access rules to what comes back.
- Brain results add to what the user told you; they never replace it. A lookup is one step: finish the whole task.
<!-- gbrain:brain-first:end -->
