# Logo Assets

The Site Builder copies logo variants from this directory into each generated site's `assets/` folder for use in the footer attribution.

## Expected Files

| Filename | Use on |
|---|---|
| `benchmuse-logo-dark.png` | Light backgrounds |
| `benchmuse-logo-light.png` | Dark backgrounds |
| `benchmuse-logo-contrast.png` | Mid-value / photo backgrounds (optional) |

SVG equivalents (`benchmuse-logo-dark.svg`, etc.) will be used preferentially if present.

## Format

- **PNG with transparency**, or SVG.
- Display size in the footer is ~18–22 px tall.
- Export PNGs at 2× or 3× display size for Retina screens.
- Target under 10 KB per file.

## Missing Variants

If none of these files exist, the footer renders a text-only "Built with BenchMuse" link. Adding variants later is additive — no other changes needed.
