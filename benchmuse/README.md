# BenchMuse Brand Assets

Logo files used in the "Built with BenchMuse" footer attribution on every generated site. The Site Builder copies the appropriate variant into each site's `assets/` directory during build.

This directory holds BenchMuse's own brand identity — it is separate from `templates/` (per-project starter files a luthier customizes) and from any `brand/` directory a luthier might create for their own business assets.

## Expected Files

| Filename | Use on |
|---|---|
| `benchmuse-logo-dark.png` | Light backgrounds |
| `benchmuse-logo-light.png` | Dark backgrounds |

SVG equivalents (`benchmuse-logo-dark.svg`, etc.) will be used preferentially if present.

## Format

- **PNG with transparency**, or SVG.
- Display size in the footer is ~18–22 px tall.
- Export PNGs at 2× or 3× display size for Retina screens.
- Target under 10 KB per file.

## Missing Variants

If neither file exists, the footer renders a text-only "Built with BenchMuse" link. Adding variants later is additive — no other changes needed.
