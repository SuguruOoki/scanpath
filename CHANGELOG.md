# Changelog

## 0.3.0 (2026-10-04)

- Renamed from Review Radar to **scanpath** — the reading path through a Git diff. The repository, CLI binary (`scanpath`), default output directory (`.scanpath/`), config template (`scanpath.config.json`), environment variable (`SCANPATH_JEV_ENDPOINT`), report branding, and the bundled agent skill (`skills/scanpath/`) all use the new name. Report ids now use the `sp-` prefix.

## 0.2.1 (2026-10-03)

- Output-path security check now rejects only a symlinked output directory itself, not symlinked ancestors — the default temporary directory on macOS (`/var` → `/private/var`) no longer makes the tool refuse to write. All tests pass on macOS.
- `design-unchecked-arithmetic` no longer treats hyphenated words (`review-priority`) as arithmetic; subtraction now requires whitespace around the minus.
- The demo fixture gained a design-lens example (removed precondition guard, side-effect write, deep property chain) and `examples/demo` outputs were regenerated.
- peco-style README in English and Japanese, plus CONTRIBUTING, CHANGELOG, SECURITY, issue/PR templates, and a bundled `design-for-reading-review` skill.
- Demo assets: English and Japanese terminal story GIFs (harmless-looking diff triaged into mandatory candidates, no wrapped lines) and an interactive report tour GIF captured at 1440px (filter, evidence expansion, search).

## 0.2.0 (2026-10-02)

- Design-lens signals: `design-contract-removed`, `design-side-effect-write`, `design-unchecked-arithmetic`, `design-stringly-typed`, `design-leaky-abstraction`, with a new `design` focus and review questions. Design signals raise the human-judgment axis (guard removal also raises failure impact).
- Detectors gained per-line direction (added/removed), test-file skipping, and compound predicates.

## 0.1.0 (2026-09-18)

- Initial release: hunk-based triage, mandatory and heuristic signals, five score axes, HTML/Markdown/JSON reports, opt-in Jev / TypeSafe scoring, feedback/evaluate/rerank, demo command.
