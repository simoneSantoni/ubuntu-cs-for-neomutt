# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A collection of NeoMutt color schemes. NeoMutt is a terminal email client; each scheme is a standalone `.neomuttrc` fragment that the user `source`s from their main config.

## Repository Structure

One subdirectory per scheme (`yaru/`, `duotone/`, `meadow/`, `github-light/`). Most schemes ship two variants:

- **Truecolor** — uses 24-bit hex values (e.g. `#192834`). Requires `set color_directcolor = yes` in the user's `neomuttrc` before sourcing.
- **256-color** — uses indexed `colorNNN` values as a fallback for terminals without 24-bit support.

File naming is **not** consistent across schemes:

- `meadow/` uses `meadow.neomuttrc` (truecolor) and `meadow-256.neomuttrc` (256). This is the preferred pattern for new schemes.
- `yaru/` uses `mutt-colors-ubuntu-yaru-truecolor.neomuttrc` and `mutt-colors-ubuntu-yaru-256.neomuttrc` (legacy).
- `duotone/` and `github-light/` ship a single truecolor file only.

When adding a new scheme, also update `README.md` (palette table + installation snippet).

## NeoMutt Color Syntax

```
color <object> <foreground> <background> [<pattern>]
```

Common objects: `normal`, `error`, `status`, `indicator`, `tree`, `sidebar_*`, `index`, `header`, `hdrdefault`, `quoted`, `quoted1-4`, `body`, `compose`, `attachment`, `signature`.

`mono` rules (e.g. `mono bold bold`) provide a fallback for monochrome terminals and should be preserved when editing.

### Index pattern coloring

Most per-message styling lives on `color index` lines whose final argument is a NeoMutt search pattern. Knowing these is essential when the user asks to recolor a message state:

| Pattern    | Meaning                                  |
|------------|------------------------------------------|
| `~A`       | all messages (default)                   |
| `~N`       | new messages                             |
| `~O`       | old messages                             |
| `~U`       | unread messages                          |
| `~U~$`     | unread, unreferenced                     |
| `~R`       | read messages                            |
| `~Q`       | replied to                               |
| `~F`       | flagged                                  |
| `~D`       | deleted                                  |
| `~E`       | expired                                  |
| `~P`       | from me                                  |
| `~p`       | to me                                    |
| `~v`       | inside a collapsed thread                |
| `~v~(...)` | collapsed thread containing matches      |

Patterns combine (e.g. `~N~F~p` = new flagged messages to me). Order in the file matters — later rules override earlier ones for the same message.

## Editing Conventions

- When changing a color across a scheme, edit **both** the truecolor and 256-color files in lockstep so the variants stay visually equivalent. Each 256 file has a hex→`colorNNN` mapping table in its header comment — use it.
- Keep the palette comment block at the top of each truecolor file in sync with the actual values used below it.
- Do not introduce new colors without adding them to the header palette comment.

## Testing

```bash
neomutt -F /path/to/<scheme>/<file>.neomuttrc
```

This launches NeoMutt with only the scheme's rules, bypassing the user's main config — useful for verifying a change in isolation.
