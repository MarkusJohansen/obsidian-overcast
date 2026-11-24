# Overcast

A low-glare Obsidian theme for long reading sessions. It has a dark mode and a light mode, and neither one uses pure black or pure white.

## Why

I made this theme because high-contrast dark themes, with bright white text on a black background, gave me eye strain. Most dark themes push contrast close to the maximum of 21:1. That is very legible, but on a dark background bright letters tend to *halate*: they seem to glow and blur at the edges, and after an hour your eyes feel it. Pure white backgrounds have the opposite problem and glare.

Overcast is named after the light on a cloudy day: soft and even, with no hard glare. Every colour and spacing value comes from readability guidance, not taste alone.

## Design

### Colour: enough contrast, not maximum contrast

The WCAG accessibility guidelines ask for at least 4.5:1 contrast for body text, and 7:1 for their strictest level (AAA). Overcast keeps body text above 7:1 and stays well below 21:1.

| | Dark | Light |
|---|---|---|
| Page | `#25272a` charcoal | `#f3efe6` warm off-white |
| Body text | `#d6d2c8` soft off-white, **9.9:1** | `#2e2c28` warm charcoal, **12.1:1** |
| Muted text | `#a39f96`, 5.7:1 | `#5f5b53`, 5.9:1 |
| Faint text (metadata only) | `#7e7b74`, 3.5:1 | `#8a857b`, 3.2:1 |
| Links | `#8fb3c9` dusty blue, 6.7:1 | `#37627f` steel blue, 5.7:1 |

- **Warm light mode.** A slightly warm off-white page glares less than pure white.
- **Charcoal dark mode.** A charcoal page with off-white text avoids halation.
- **Muted accents.** Accents and callout colours are desaturated, and so are Obsidian's built-in named colours, so graphs, canvases and inline charts match.
- **Headings without colour.** Headings stand out by size and weight only. Each change of colour makes the eye readjust.
- **Selection and highlights.** These are soft translucent tints, not solid blocks.

### Typography

| Setting | Value | Guidance it follows |
|---|---|---|
| Font | Inter, falling back to SF Pro or the system sans | Tall x-height (lowercase letters are large next to capitals), open shapes in c, e and a, even stroke width |
| Size | 17px | 16–18px for reading on a desktop |
| Weight | 400 for body text, 600 for bold | Regular weight for body text. Light weights lose contrast, and heavy bold slows continuous reading |
| Line height | 1.6 | 1.4–1.6, so the eye doesn't slip back onto the same line |
| Line length | 36rem, about 65–70 characters | 50–75 characters, which keeps the jump back to the start of each line short |

Two smaller details:
- **Clear I, l and 1.** Inter's alternate letter shapes are switched on: a lowercase l with a tail (`cv05`) and a capital I with serifs (`cv08`), so the three never look alike.
- **Dark-mode text.** Light text on a dark background looks heavier than it is. Dark mode adds a little letter spacing and lighter font smoothing to keep letters crisp.

The theme only sets CSS variables, plus a few small rules for text rendering. It doesn't override layout, so it should keep working through Obsidian updates.

## Install

1. Install [Inter](https://rsms.me/inter/). On macOS you can run `brew install --cask font-inter`. Without it, the theme falls back to the system sans-serif.
2. Copy `manifest.json` and `theme.css` into `<your vault>/.obsidian/themes/Overcast/`.
3. In Obsidian, open Settings → Appearance → Themes and choose **Overcast**. Restart Obsidian if you have just installed Inter.

If your sidebars look washed out, turn off **Translucent window** under Settings → Appearance. With it on, a bright desktop wallpaper shows through the sidebars and brings the glare back.
