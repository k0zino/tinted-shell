# Tint my Shell — GNOME Shell 51 fork

> **This is a fork of [pakovm-git/tinted-shell](https://github.com/pakovm-git/tinted-shell)
> with GNOME Shell 51 support.**

Tints GNOME Shell elements with the system accent color while preserving the original
visual style.

## GNOME Shell 51 port

The upstream extension targets GNOME Shell 48–50. This fork adds 51 support:

- `metadata.json` now lists `"51"` in `shell-version` and keeps `unlock-dialog`
  session mode so the lock screen is tinted as well.
- `stylesheet.css` was regenerated from GNOME Shell 51's stock
  `gnome-shell-dark.css`, mixing 10% of `-st-accent-color` into every surface
  color while preserving upstream's lightness and
  hover/active/checked/insensitive states.
- New GNOME 51 widgets are covered (login dialog, parental controls, lock screen,
  workspace dot, screenshot UI, ...).
- An invalid `st-mix(-st-accent-color, transparent !important, 10%)` declaration
  from the old stylesheet was fixed.

## Install

```bash
gnome-extensions pack .
# or copy this directory to:
# ~/.local/share/gnome-shell/extensions/tinted-shell@pakovm/
```

Then enable it:

```bash
gnome-extensions enable tinted-shell@pakovm
```

## Notes

- The stylesheet is generated for GNOME Shell's **dark** theme, matching the
  upstream extension's behavior.
- For a version that also tints libadwaita/GTK4 applications, see
  [Tint-my-Gnome](https://github.com/k0zino/Tint-my-Gnome).

## License

Same as upstream. See `LICENSE`.
