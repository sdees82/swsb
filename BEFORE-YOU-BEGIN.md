# How to use the book and companion

This walkthrough is for one engineer directing one agent through a local project. You create and maintain the Markdown guidance. The agent creates the application source, configuration and tests. You review and accept that work; you do not manually create TS or TSX files.

## Obtain the matching revision

Get the companion at https://github.com/sdees82/swsb. Use VERSION.md to match the package to your book edition. MANIFEST.md gives file sizes and SHA-256 checksums; ask the agent to compare the downloaded inventory before setup. The repository README carries setup updates and the route for reporting corrections.

## Prerequisites

Use a computer with a terminal, Git, Node and npm, a browser with WebGL, and one signed-in coding harness: Claude Code or Codex. Choose one. SETUP.md records runtime and dependency versions; no second subscription or browser-automation tool is required. Run node --version, npm --version and git --version yourself. Compare Node with the supported version in SETUP.md. Confirm that a local browser can use WebGL. If it cannot, the app's fallback can be checked, but the visible 3D criteria stay open until a capable browser is available.

## Folders and responsibilities

Keep this structure, with both folders under a workspace you control:

```text
workspace/
  swsb/                  guidance and assets; read-only to the agent
    VERSION.md
    SETUP.md
    MILESTONES.md
    MODEL-INSPECTION.md
    starter/
    teaching/
  my-ring-builder/       your new working project
    AGENTS.md
    docs/specs/first-preview.md
```

Create the empty working folder. Copy starter/AGENTS.md into its root and teaching/docs/specs/first-preview.md into docs/specs/first-preview.md. These are Markdown you review. Chapter 1 adds docs/preview-outcome.md. The agent copies model/font/JSON assets during the authorized Chapter 3 practice rep. There is no supplied application, package manifest, lockfile, decoder, executable script or passing test suite.

## Choose one launch path

Claude Code: from my-ring-builder, launch `claude --permission-mode plan --add-dir ../swsb` for Chapter 2. The added directory grants access, not a read-only boundary by itself. Keep the task read-only, inspect permissions and reject writes. If your version loads AGENTS.md directly, confirm it in the context display. Otherwise create a root CLAUDE.md containing only `@AGENTS.md`; never maintain a second briefing. Version-dependent details are linked in SOURCES.md. Switch to a write-capable local session only after the authority preflight.

Codex CLI: from my-ring-builder, launch `codex --sandbox read-only` for Chapter 2. Ask it to read `../swsb/SETUP.md` explicitly. Do not use --add-dir merely to read the companion: in Codex that flag adds writable directories. If the sandbox cannot read the sibling folder, stop and adjust the read boundary in your supported environment, or copy only the required Markdown into a read-only reference folder inside the project and record its revision. Begin a workspace-write session only after the authority preflight. In the Codex desktop app, open my-ring-builder and select equivalent read-only permissions; verify the actual scope in the app rather than assuming CLI flags configure it.

## Confirm the starting state

The Chapter 2 answer must (1) cite the actual companion revision and model path, (2) distinguish supplied Markdown/assets from app outputs, (3) explain PV-01–05, (4) preserve the fixed stack and local boundary, and (5) report that no implementation or passing suite exists yet. No files should change during that session.

## Recovery

Wrong working directory: stop and reopen my-ring-builder. Sibling access denied: correct only that read boundary; do not grant whole-disk writes. Missing Node or sign-in: follow the vendor setup linked in SOURCES.md, then repeat the prerequisite checks. Missing asset or mismatched JSON: restore the complete matching companion revision. Dependency resolution failure: retain the npm output and ask for a decision before changing the recorded stack. Model-load failure: check local HTTP, /models and /draco requests before replacing assets. Missing browser tools: you perform the printed interactions and record them as reader observations. A failed or unavailable check stays open.


## Feature specification timing

At the beginning of Chapter 4, copy player-personalization.md, ring-logo.md and material-customization.md from teaching/docs/specs/ into my-ring-builder/docs/specs/. Review Player first; keep the logo and material specs inactive until their Chapter 5 loops. Follow teaching/templates/evidence-paths.md for the working-project evidence records.
