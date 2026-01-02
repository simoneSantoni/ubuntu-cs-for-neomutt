# Ubuntu Yaru Color Scheme for NeoMutt

A color scheme for [NeoMutt](https://neomutt.org/) inspired by the [Ubuntu Yaru](https://github.com/ubuntu/yaru) color palette, featuring the iconic eggplant/aubergine tones.

## Features

- Full styling for all NeoMutt UI elements (index, sidebar, headers, compose view)
- Distinct colors for message states (new, read, flagged, deleted)
- Quoted text levels with different colors
- URL and email address highlighting
- GPG/PGP signature status coloring
- Two versions available:
  - **256-color** - Works in most terminals
  - **True color** - Uses exact hex values for terminals with 24-bit color support

## Color Palette

| Color           | Hex       | Usage                          |
|-----------------|-----------|--------------------------------|
| Eggplant (bg)   | `#2C001E` | Background                     |
| Aubergine       | `#772953` | Accents, replied messages      |
| Orange          | `#E95420` | Ubuntu orange, links, indicator|
| Gold            | `#F99B15` | Dates, warnings                |
| Green           | `#26A269` | Messages to me, good signature |
| Teal            | `#19B6EE` | New/unread messages, subjects  |
| Red             | `#C7162B` | Flagged, deleted, errors       |
| Foreground      | `#F6F5F4` | Normal text                    |

## Installation

### 256-color version

Add to your `neomuttrc`:

```neomuttrc
source /path/to/mutt-colors-ubuntu-yaru-256.neomuttrc
```

### True color version

Requires a terminal with 24-bit color support. Add to your `neomuttrc`:

```neomuttrc
set color_directcolor = yes
source /path/to/mutt-colors-ubuntu-yaru-truecolor.neomuttrc
```

## Testing

Test the color scheme without modifying your config:

```bash
neomutt -F /path/to/mutt-colors-ubuntu-yaru-256.neomuttrc
```

## Credits

Based on [yaru.nvim](https://github.com/simoneSantoni/yaru.nvim) by Simone Santoni.

## License

MIT
