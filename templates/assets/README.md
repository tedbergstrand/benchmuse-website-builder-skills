# BenchMuse Logo Assets

This folder holds the BenchMuse logo variants that the Site Builder skill
copies into every generated website's `assets/` directory for use in the
"Built with BenchMuse" footer attribution.

## Expected Files

| Filename | When Used | Notes |
|---|---|---|
| `benchmuse-logo-dark.png` | On **light** backgrounds (cream, paper, white) | Logo rendered in dark ink. The most common case. |
| `benchmuse-logo-light.png` | On **dark** backgrounds (ink, slate, warm brown) | Logo rendered in cream/white. Used when the footer is a dark band — which is most of the generated sites. |
| `benchmuse-logo-contrast.png` | On **mid-value** backgrounds where neither pure dark nor pure light reads cleanly | Optional. Logo with an outline or subtle halo so it reads on gray, beige, or photo-backed footers. The Site Builder will fall back to this if the detected footer background is ambiguous. |

## Format & Size Recommendations

- **PNG with transparency** — not JPG. The logo will sit on colored footer backgrounds that aren't pure white.
- **Target display size is ~18–24px tall** inline with the footer text.
- **Export at 2× or 3× that size** (so 72–96px tall source) for crisp rendering on Retina / high-DPI screens.
- Keep the file under 10 KB each if possible — these load on every page of every generated site.
- If you later produce an SVG version, drop in `benchmuse-logo-dark.svg` / `benchmuse-logo-light.svg` alongside the PNGs. The Site Builder will prefer SVG if present (it scales perfectly and is often smaller).

## Graceful Degradation

The Site Builder is written to tolerate missing files — if none of these variants exist, the footer will render a text-only "Built with BenchMuse" link instead of failing. So it's safe to add variants over time as you produce them.
