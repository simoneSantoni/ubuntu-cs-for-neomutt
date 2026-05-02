# NeoMutt Color Schemes

A collection of color schemes for [NeoMutt](https://neomutt.org/), a command-line email client.

## Color Schemes

### Yaru (`yaru/`)

Inspired by the [Ubuntu Yaru](https://github.com/ubuntu/yaru) color palette, featuring the iconic eggplant/aubergine tones.

- Full styling for all NeoMutt UI elements (index, sidebar, headers, compose view)
- Distinct colors for message states (new, read, flagged, deleted)
- Quoted text levels with different colors
- URL and email address highlighting
- GPG/PGP signature status coloring
- Two versions available:
  - **256-color** - Works in most terminals
  - **True color** - Uses exact hex values for terminals with 24-bit color support

#### Color Palette

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

#### Installation

**256-color version** - add to your `neomuttrc`:

```neomuttrc
source /path/to/yaru/mutt-colors-ubuntu-yaru-256.neomuttrc
```

**True color version** - requires a terminal with 24-bit color support:

```neomuttrc
set color_directcolor = yes
source /path/to/yaru/mutt-colors-ubuntu-yaru-truecolor.neomuttrc
```

### Duotone (`duotone/`)

A duotone theme featuring teal/turquoise with bright field green, based on [Base2Tone Field Dark](https://github.com/atelierbram/Base2Tone-kitty) by Bram de Haan.

- True color only (requires 24-bit color support)
- Teal-gray dark background with green/cyan accent tones
- Full styling for all NeoMutt UI elements

#### Color Palette

| Color           | Hex       | Usage                          |
|-----------------|-----------|--------------------------------|
| Dark teal-gray  | `#18201e` | Background                     |
| Teal            | `#0fbda0` | Primary accent, URLs, indicator|
| Bright teal     | `#25d0b4` | Messages to me                 |
| Cyan            | `#40ddc3` | Old messages, quoted text      |
| Bright cyan     | `#88f2e0` | New/unread messages, subjects  |
| Green           | `#3be381` | Tree, good signatures          |
| Bright green    | `#55ec94` | Flagged messages, errors       |
| Mint            | `#85ffb8` | Expired, search highlight      |
| Foreground      | `#8ea4a0` | Normal text                    |

#### Installation

Requires a terminal with 24-bit color support. Add to your `neomuttrc`:

```neomuttrc
set color_directcolor = yes
source /path/to/duotone/duotone.neomuttrc
```

### Meadow (`meadow/`)

A duotone theme featuring a slate-blue background with bright lime green and green accents, based on [Base2Tone Meadow Dark](https://github.com/atelierbram/Base2Tone-kitty) by Bram de Haan.

- Slate-blue background with layered green/lime accents
- Lime accent for unread, expired, and high-priority states
- Full styling for all NeoMutt UI elements (index, sidebar, headers, compose view)
- Two versions available:
  - **256-color** - Works in most terminals
  - **True color** - Uses exact hex values for terminals with 24-bit color support

#### Color Palette

| Color           | Hex       | Usage                          |
|-----------------|-----------|--------------------------------|
| Slate blue (bg) | `#192834` | Background                     |
| Selection       | `#223644` | Collapsed-thread highlight     |
| Border          | `#466b86` | Tildes, dividers               |
| Foreground      | `#7b9eb7` | Normal text, "From" header     |
| Dim slate       | `#3d5e76` | Replied, signatures, comments  |
| Light blue      | `#afddfe` | New messages, subjects         |
| Blue            | `#4299d7` | Old messages, primary quoted   |
| Green           | `#80bf40` | Messages to me, "To" header    |
| Bright green    | `#8cdd3c` | Flagged, indicator, markers    |
| Lime            | `#a6f655` | Unread, expired, "Date" header |
| White           | `#fafbf9` | Status bar, bold/underline     |

#### Installation

**256-color version** - add to your `neomuttrc`:

```neomuttrc
source /path/to/meadow/meadow-256.neomuttrc
```

**True color version** - requires a terminal with 24-bit color support:

```neomuttrc
set color_directcolor = yes
source /path/to/meadow/meadow.neomuttrc
```

### GitHub Light (`github-light/`)

A light theme matching the GitHub website's light mode, based on [github-nvim-theme](https://github.com/projekt0n/github-nvim-theme) by projekt0n.

- True color only (requires 24-bit color support)
- White background with GitHub-style blue/green/red accents
- Full styling for all NeoMutt UI elements

#### Color Palette

| Color           | Hex       | Usage                          |
|-----------------|-----------|--------------------------------|
| White (bg)      | `#ffffff` | Background                     |
| Subtle bg       | `#f6f8fa` | Status bar, markers            |
| Foreground      | `#1f2328` | Normal text                    |
| Comment         | `#6e7781` | Read messages, signatures      |
| Blue            | `#0969da` | New/unread, subjects, indicator|
| Green           | `#1a7f37` | Messages to me, "To" header    |
| Yellow          | `#9a6700` | Expired, "Date", emoticons     |
| Orange          | `#e8590c` | URLs                           |
| Red             | `#cf222e` | Flagged, deleted, errors       |
| Purple          | `#8250df` | Replied messages               |
| Selection       | `#add6ff` | Search highlight, sidebar      |

#### Installation

Requires a terminal with 24-bit color support. Add to your `neomuttrc`:

```neomuttrc
set color_directcolor = yes
source /path/to/github-light/github-light.neomuttrc
```

## Testing

Test a color scheme without modifying your config:

```bash
neomutt -F /path/to/yaru/mutt-colors-ubuntu-yaru-256.neomuttrc
```

## Credits

- Yaru scheme based on [yaru.nvim](https://github.com/simoneSantoni/yaru.nvim) by Simone Santoni.
- Duotone scheme based on [Base2Tone-kitty](https://github.com/atelierbram/Base2Tone-kitty) by Bram de Haan.
- Meadow scheme based on [Base2Tone-kitty](https://github.com/atelierbram/Base2Tone-kitty) by Bram de Haan.
- GitHub Light scheme based on [github-nvim-theme](https://github.com/projekt0n/github-nvim-theme) by projekt0n.

## License

MIT
