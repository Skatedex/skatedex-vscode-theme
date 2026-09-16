# Skatedex for VS Code

Created by Kyle Niedzwiecki. Copyright 2026 Skatedex LLC.

Two color themes built on the Skatedex app palette, so the editor matches the product.

- **Skatedex Night** is the dark variant. The editor sits on `#0D1117`, sampled from skatedex.com's dark mode.
- **Skatedex Day** is the light variant. The editor sits on `#F7F9FB`, the app canvas.

## Palette

Night is sampled from skatedex.com's dark mode and stays inside blue, gray, white, and black. Syntax is separated by tone rather than hue.

| Role | Night | Day |
| --- | --- | --- |
| Editor canvas | `#0D1117` | `#F7F9FB` |
| Chrome (sidebar, tabs, panel, terminal) | `#0C141F` | `#EEF2F6` |
| Elevated surfaces (widgets, hover) | `#171B21` | `#FFFFFF` |
| Accent (buttons, badges, tab rail) | `#4190C5` | `#4190C5` |
| Default text, variables, punctuation | `#AEBAC6` gray | `#4F6272` slate |
| Keywords, tags, CSS selectors, headings | `#4FA3E3` vivid blue | `#1479C9` vivid blue |
| Functions, properties, attributes, types | `#FFFFFF` (types bold) | `#14232E` (types bold) |
| Strings, CSS values | `#BFE0FA` ice | `#234B6E` navy |
| Numbers, constants, booleans | `#7FC0EE` mid blue | `#2F7FC4` mid blue |
| Comments | `#5F6F80` italic | `#8A9BAB` italic |

The ladder works by lightness, not hue. Default text is deliberately dimmed so that names (white / near-black) and keywords (saturated blue) carry the structure, and strings sit one step off the names so long values read as data rather than code.

Red `#E0483E` appears only where it has to: errors, deletions, breakpoints. A muted sand `#D9A441` is used for warning squiggles only, so warnings stay tellable from info. Terminal ANSI green, yellow, and magenta are kept but desaturated, since shell output relies on them meaning what they mean.

## Install locally

```bash
# macOS / Linux
cp -r skatedex-theme ~/.vscode/extensions/

# Windows
xcopy skatedex-theme %USERPROFILE%\.vscode\extensions\skatedex-theme /E /I
```

Restart VS Code, then `Cmd/Ctrl + K` `Cmd/Ctrl + T` and pick Skatedex Night or Skatedex Day.

## Tweaking

Both themes are plain JSON. `colors` drives the workbench chrome, `tokenColors` drives TextMate syntax scopes, and `semanticTokenColors` drives language-server highlighting, which takes priority when a language supports it. To change how something looks, run **Developer: Inspect Editor Tokens and Scopes** from the command palette with your cursor on the token, then edit the matching scope.

## License and credits

Copyright 2026 Skatedex LLC. Released under the MIT License, see LICENSE.md.

Created by Kyle Niedzwiecki for Skatedex, https://skatedex.com.
