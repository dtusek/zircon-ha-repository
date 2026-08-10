# Codex workflow

Default to minimal-context work.

- Start from the named file, symbol, feature, error, or command; do not scan the whole repository by default.
- Use targeted search (`rg`, exact paths, focused queries) before reading broad docs.
- Read only files required for the task. Avoid recursive reads of docs, examples, fixtures, generated assets, build output, logs, archives, snapshots, vendored code, and dependency trees unless necessary.
- Do not invoke sub-agents or broad research unless explicitly requested or clearly necessary.
- Prefer one implementation pass plus targeted verification; do not repeatedly re-read unchanged files.
- Run the smallest relevant test/lint/build target first; use full suites only for cross-cutting changes.
- Preserve upstream/project conventions and avoid unrelated refactors.
- Before edits, check `git status -sb`; never overwrite unrelated work or use destructive git commands without explicit approval.

Modes: `LOW` is default; `NORMAL` may inspect directly related modules/tests; `DEEP` is only for explicitly requested or genuinely repository-wide work.

Completion: report only what changed, files changed, checks run, and real remaining risks.