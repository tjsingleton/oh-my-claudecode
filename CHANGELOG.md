# oh-my-claudecode v4.14.2: safer cleanup, durable ultragoal, plugin/runtime hardening

## Release Notes

Patch release with **16 user-facing fixes / hardening changes** across destructive worktree cleanup safety, durable Ultragoal state, Claude goal activation, plugin cache repair, HUD warnings, Windows runtime support, team spawning, and generated-artifact hygiene.

### Highlights

- **Safer destructive cleanup** (#3103, #3091) — guard worktree cleanup and teleport removal paths so destructive operations require safer path validation and fallbacks.
- **Durable Ultragoal + Claude goal activation** (#3102) — persist Ultragoal story ledgers and enforce the Claude goal activation handoff before execution proceeds.
- **Plugin and runtime reliability** (#3080, #3072) — keep command wrappers materialized in repaired plugin caches and keep Claude plugin registries aligned after update.
- **Team/HUD/Windows hardening** (#3074) — warn before HUD payload pressure blindsides sessions, fix cmux team worker spawning, and harden Windows HUD / PowerShell startup paths.

### New Features

- **Persist Ultragoal and enforce Claude goal activation** (#3102).
- **Add model × agent compatibility and recommendation matrix** (#3092, #3094).

### Bug Fixes & Hardening

- Guard destructive worktree cleanup paths (#3103).
- Fix unsafe teleport remove fallback (#3091).
- Fix Windows HUD git execution.
- Preserve plugin command wrappers in repaired cache payloads (#3080).
- Fix stale plugin cache repair after marketplace updates.
- Fix psmux PowerShell worker startup on native Windows.
- Warn before HUD payload pressure blindsides sessions (#3074).
- Keep Claude plugin registry aligned after update (#3072).
- Fix cmux team worker spawning.
- Avoid release-like HUD cache test fixtures (#3067).

### Cleanup & Build Hygiene

- Remove residual slop after source-overall cleanup.
- Keep cleanup artifacts whitespace-clean.
- Preserve provenance release workflow during cleanup.
- Keep verification gates portable after dependency audit.
- Record cleanup lane ownership, fallback inventory, and generated artifact policy for future safe cleanup batches.

### Stats

- **29 commits since v4.14.1** | **9 PRs analyzed** | **patch release** | **safety, goal workflow, plugin cache, HUD, Windows, and team runtime hardening**

### Install / Update

```bash
npm install -g oh-my-claude-sisyphus@4.14.2
```

Or reinstall the plugin:
```bash
claude /install-plugin oh-my-claudecode
```

**Full Changelog**: https://github.com/Yeachan-Heo/oh-my-claudecode/compare/v4.14.1...v4.14.2

## Contributors

Thank you to all contributors who made this release possible!

@Yeachan-Heo
