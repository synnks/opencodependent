# OpenCodependent

[`README.md`](README.md) describes the project and its architecture.

## Build and Code Style

- Keep the project as a single Bun/TypeScript package; add dependencies and abstractions when the current work needs them.
- Put dependencies and scripts in `package.json` and compiler settings in `tsconfig.json`.
- Use the Effect-native plugin API from `@opencode/plugin/effect` and public SDK interfaces rather than OpenCode Core internals.
- Use Prettier for source and configuration files; `.prettierrc.json` defines the style.
- Keep the README focused on project purpose, architecture, and supported behavior; keep contributor guidance here.
- Document current behavior and usage in READMEs; keep roadmap notes and change history out.
- Use semantic line breaks for Markdown prose, with one sentence per line.

## Testing and Validation

Install the pinned dependencies with `bun install --frozen-lockfile`.
Format source and configuration with `bun run format`; check them with `bun run format:check`.
Start with the smallest affected test suite and typechecks when available.
For documentation-only changes, check relative links and whitespace.

## Agent Configuration

- Shared agent configuration belongs in `AGENTS.md` and `.agents/`.
- Vendor-specific configuration such as `.claude/`, `.cursor/`, and `.opencode/` stays local and ignored.
