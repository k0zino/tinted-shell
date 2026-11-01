# Tint my Shell 51

Tints GNOME Shell 51 elements with the system accent color while preserving the
original visual style.

This is an unofficial GNOME Shell 51 port of
[Tint my Shell](https://github.com/pakovm-git/tinted-shell) by
[PakoVM](https://github.com/pakovm-git). All credit for the original design and
implementation goes to the original author.

## What it does

- Uses the system accent color (`-st-accent-color`) and mixes 10% of it into
  GNOME Shell surfaces.
- Keeps the original lightness and hover/active/checked/insensitive states.
- Covers GNOME Shell 51 widgets, including the login dialog, parental controls,
  lock screen, workspace indicator and screenshot UI.
- Keeps dash icons transparent so Dash to Dock can draw its own highlight.

The accent color is controlled by **GNOME Settings → Appearance → Accent Color**.
There is no per-extension color setting.

## Install

```bash
gnome-extensions install --force tinted-shell-51@k0zino.shell-extension.zip
gnome-extensions enable tinted-shell-51@k0zino
```

Or copy this directory to:

```text
~/.local/share/gnome-shell/extensions/tinted-shell-51@k0zino/
```

## Compatibility

- GNOME Shell 51.x
- Dark shell theme (the same limitation as the original extension)

## License

GPL-3.0. See `LICENSE`.
