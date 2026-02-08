# Atlas GitHub Toolkit

GitHub organization toolkit built on Atlas CLI patterns - a deterministic tool layer for AI agents to manage GitHub at org scale.

## Relationship to Atlas

This repository is a standalone development home for GitHub tooling that will merge into `~/Projects/Atlas/` as the `atlas github` command group once stable.

## Architecture

- Uses Atlas CLI conventions (`ParsedArguments`, `ToolRegistry`, `ToolRuntime`)
- Policy enforcement for mutating operations (`read_only_safe` vs `mutating_needs_approval`)
- JSONL audit logging for all GitHub operations
- GitHub operations via `gh` CLI (GraphQL where needed), no embedded intelligence

## Planned Command Surface

- `atlas github triage-summary`
- `atlas github project-status`
- `atlas github milestone-summary`
- `atlas github archival-status`
- `atlas github issue list|create|update`
- `atlas github repo archive`
- `atlas github labels sync`
- `atlas github weekly-report`

## Legacy Assets

- `.claude/commands/generic` contains workflow playbooks (gh-work, gh-finish, create-issue, review-pr) to be ported into Atlas tools and/or the `~/.agents` hub.
- `docs/prd.md` captures the original roadmap and command inventory for porting.

## Development Status

Planning phase. Implementation not started.

## Related Projects

- [Atlas](../Atlas/README.md) - Parent project this will merge into
- [Atlas-weekly-planner](../Atlas-weekly-planner/README.md) - Parallel Atlas subcommand project
- [copilot-config](../copilot-config/README.md) - Orchestrator config used by agents
- [Projects Index](../README.md) - Full portfolio overview
