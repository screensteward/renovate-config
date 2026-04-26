# screensteward / renovate-config

Shared Renovate presets for the [ScreenSteward](https://github.com/screensteward) repos.

This repo holds no code — only Renovate configuration. It is consumed by every ScreenSteward repo (GitHub public + GitLab private self-hosted) via:

```json
{
  "extends": ["github>screensteward/renovate-config"]
}
```

## Presets

- `default.json` — base preset, automerge matrix, grouping, schedule. All other presets extend it.
- `dart.json` — Dart / pub.dev specific overrides.
- `rust.json` — Cargo / crates.io specific overrides.
- `python.json` — Python / PyPI / pyproject overrides.
- `flutter.json` — Flutter UI repo overrides (combines Dart + post-upgrade `gen-l10n`).

## Versioning

Tagged with `vX.Y.Z`. Repos pin to a tag for stability:

```json
{
  "extends": ["github>screensteward/renovate-config#v1.0.0"]
}
```

Or float on the latest:

```json
{
  "extends": ["github>screensteward/renovate-config"]
}
```

ScreenSteward repos float on the latest by convention (cf. `screensteward-docs/conventions/dependencies.md`).

## License

MIT. Configuration is not a derivative work of the projects it monitors.
