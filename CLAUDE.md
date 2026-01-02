# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains a NeoMutt color scheme inspired by the Ubuntu Yaru color palette. NeoMutt is a command-line email client.

## File Structure

- `mutt-colors-ubuntu-yaru-256.neomuttrc` - Color scheme using 256-color mode with hex backgrounds
- `mutt-colors-ubuntu-yaru-truecolor.neomuttrc` - Color scheme using true color (24-bit) hex values throughout

Both files style the same NeoMutt elements but differ in color specification format.

## Ubuntu-Yaru Color Palette

| Color Name      | Hex Value | 256-color Approx |
|-----------------|-----------|------------------|
| bg (eggplant)   | #2C001E   | -                |
| bg_alt          | #3B1028   | -                |
| fg              | #F6F5F4   | color255         |
| fg_dim          | #D5CFCA   | color251         |
| comment         | #B7A7B4   | color249         |
| orange          | #E95420   | color202         |
| aubergine       | #772953   | color89          |
| aubergine_dark  | #5E2750   | -                |
| gold            | #F99B15   | color214         |
| green           | #26A269   | color35          |
| teal            | #19B6EE   | color39          |
| red             | #C7162B   | color160         |
| border          | #4A1D33   | color89          |
| selection       | #3D1E2F   | -                |

## NeoMutt Color Scheme Syntax

```
color <object> <foreground> <background> [<pattern>]
```

Key objects styled: `normal`, `error`, `status`, `indicator`, `tree`, `sidebar_*`, `index`, `header`, `hdrdefault`, `quoted`, `quoted1-4`, `body`, `compose`.

## Testing

Source in neomuttrc:
```
source /path/to/mutt-colors-ubuntu-yaru-256.neomuttrc
```

For true color version, first enable direct color:
```
set color_directcolor = yes
source /path/to/mutt-colors-ubuntu-yaru-truecolor.neomuttrc
```

Or run directly:
```
neomutt -F /path/to/test-neomuttrc
```
