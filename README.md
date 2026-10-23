# gloss

Translate and speak text, displayed in a Wayland `osd-window` overlay.

`gloss` runs a `walker` prompt, translates the input through Google's free
endpoint, renders the full result (definitions, synonyms, examples, …) as Pango
markup, and shows it in `osd-window`. Press `s` to speak the translation and
`o` to speak the original.

## Usage

```
gloss                 # walker prompt -> translate -> osd-window
gloss --speak LANG TEXT  # read TEXT aloud in LANG
```

Language hints are the translate-shell style: `:pl`, `pl:`, or `pl:en` as the
first word of the prompt.

## Install

From a paru personal repo (see `~/.config/paru/paru.conf`):

```ini
[gloss]
Url = https://github.com/zeteref/gloss.git
Depth = 1
SkipReview
GenerateSrcinfo
```

then `paru -S gloss`.

### Dependencies

- `walker` (AUR) — the input prompt
- `curl`, `jq`, `mpv`, `python` — official repos
- `osd-window` (companion repo: github.com/zeteref/osd-window)

## Configuration

gloss uses an osd-window config at `~/.config/gloss/osd-window.toml` if present,
otherwise the packaged default at `/usr/share/gloss/osd-window.toml`.
