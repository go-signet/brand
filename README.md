# Signet brand assets

Official brand assets for [Signet](https://github.com/go-signet) — a self-hosted OAuth 2.0 / OIDC authorization server written in Go.

The identity is a **signet ring** — the original instrument for signing and certifying documents, which is exactly what Signet does for your tokens. The system uses two marks that share one geometry:

- **Full mark** (`mark.svg`): the complete ring — octagonal bezel with a carved "S" on a ring band. Use wherever there is room: README headers, websites, slides, social cards.
- **Small mark** (`icon.svg`): the bezel alone. Use at small sizes: favicons, org avatar, app icons, 16–64 px contexts where the band would collapse into a thin line.

## Files

| File | Usage |
| --- | --- |
| `logo.svg` | Full lockup (ring + wordmark) for light backgrounds |
| `logo-dark.svg` | Full lockup for dark backgrounds |
| `logo-auto.svg` | Lockup that follows `prefers-color-scheme` (websites; not GitHub READMEs) |
| `mark.svg` | Full mark, square — slides, stickers, large avatars |
| `icon.svg` | Small mark, square — favicons and tiny contexts |
| `preview.png` / `preview-dark.png` | 1200×630 social / Open Graph cards |
| `favicon/` | Generated favicon set (from the small mark) + `HEAD-snippet.html` |

The wordmark is set in [Poppins](https://fonts.google.com/specimen/Poppins) (Medium 500), converted to outlines — no font dependency.

## Palette

| Name | Hex | Usage |
| --- | --- | --- |
| Bezel indigo | `#4338CA` | Bezel fill, primary brand color |
| Band indigo | `#6366F1` | Ring band |
| Frost | `#EEF2FF` | Carved "S" strokes |
| Periwinkle | `#C7D2FE` | Hairline inner frame |
| Ink | `#1E1B2E` | Wordmark on light backgrounds |
| Cream | `#F1F2F8` | Wordmark on dark backgrounds |
| Paper | `#F5F6FB` | Light background / preview canvas |

## Light & dark mode

The marks are mode-agnostic — only the wordmark ink switches.

GitHub README snippet:

```html
<picture>
  <source media="(prefers-color-scheme: dark)"
          srcset="https://raw.githubusercontent.com/go-signet/brand/main/logo-dark.svg">
  <img alt="Signet" width="380"
       src="https://raw.githubusercontent.com/go-signet/brand/main/logo.svg">
</picture>
```

`logo-auto.svg` works when embedded on websites, but GitHub strips `<style>` from SVGs in READMEs — use the `<picture>` pattern there.

## Usage rules

- Full mark above ~64 px height; small mark below.
- Keep clear space of at least 25% of the mark's width.
- Do not recolor, add gradients or shadows, rotate the octagon, or detach the bezel from the band in the full mark.
- GitHub org avatar: `favicon/android-chrome-512x512.png` (GitHub does not accept SVG).

## License

Brand assets are released under CC BY 4.0. "Signet" and the ring mark identify the go-signet project — please don't use them to imply endorsement.
