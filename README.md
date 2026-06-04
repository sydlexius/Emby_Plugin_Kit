# Emby Plugin Kit

A cross-platform .NET toolkit that brings production-grade developer tooling to
Emby plugin developers - the dev-tooling and lessons-learned from real Emby
plugins, packaged so any plugin can adopt them.

> Status: early / design stage. Not yet usable. The design is being finalized
> before implementation begins.

## What it is

`emby-plugin-kit` (alias `epk`) is an idempotent .NET global tool that can:

- **Scaffold a new Emby plugin** (greenfield), or
- **Layer selected tooling onto an existing plugin repo** (brownfield) - safely
  and re-runnably.

Everything is driven by a single `emby-plugin-kit.toml` that enables or disables
each capability. Re-running the tool reconciles your repo to that config.

## Design principles

- **Lowest barrier:** no runtime beyond the .NET SDK you already have.
- **Brownfield-first:** incorporating the tooling into an existing repo must be
  low-friction and safe to re-run, not a one-shot generator.
- **Cross-platform:** Windows, macOS, and Linux.
- **Emby-first, adapter-ready:** host-specific behavior lives behind a host
  adapter, so a Jellyfin adapter can be added later without a rewrite.

## Planned capabilities

- C# analyzer suite (StyleCop, Roslynator, IDisposableAnalyzers, threading) + `.editorconfig`
- Git hooks (format, eslint, whitespace, gitleaks, actionlint) via lefthook
- CI-parity pre-push gate
- GitHub Actions CI scaffold
- Security suite: CodeQL, OSSF Scorecard, Dependabot + auto-approve/merge
- Release automation (category-based release notes + tag-driven releases)
- Docs site (MkDocs/ProperDocs + Pages deploy)
- Dual-ABI build matrix with automated Emby SDK reference-assembly fetch
- JS minify/embed pipeline for embedded plugin pages
- UAT harness (deploy + synthetic media + concurrency stress + API assertions)
- SharpFuzz fuzz harness
- Playwright screenshot capture with anonymization

## License

MIT. See [LICENSE](LICENSE).

## Acknowledgements

Derived from tooling proven in the
[Segment_Reporting](https://github.com/sydlexius/Segment_Reporting) Emby plugin.
