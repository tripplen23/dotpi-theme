# dotpi-theme

Themes for [dotpi](https://github.com/tripplen23/dotpi) — a Pi coding agent config.

Mounted as the `themes/` submodule of dotpi, so `~/.pi/agent/themes/` is this repo
and Pi discovers every `*.json` here with no configuration. The active theme
hot-reloads when you edit it, which is why themes live here rather than being
shipped as a Pi package (packages do not hot-reload).

## Themes

| File | Name | Look |
|---|---|---|
| `old-money.json` | `old-money` | Leather-and-brass. Walnut/ink backgrounds, brass `#f9cf5e` accent, bone text, vermilion errors, and a thinking ramp that runs dim → leather → brass → amber → vermilion. Default. |

## Adding one

1. Copy an existing file, rename it, and set `name` to match the filename.
   A name cannot contain `/` and cannot be `system`.
2. The file must define every required colour token — the
   [schema](https://github.com/earendil-works/pi/blob/main/packages/coding-agent/src/modes/interactive/theme/theme-schema.json)
   is the reference.
3. Save it here and pick it with `/theme` (or `/settings` → Theme). No reload needed
   while it is the active theme.

## Driving it from the keyboard

- `/theme` — picker over every discovered theme
- `/theme <name>` — switch directly
- `pi --use-theme <name>` — one run, without changing the saved setting
- `settings.json` → `"theme": "<name>"` — the saved default
