# marusho-design-tokens

Shared CSS design tokens for all Marusho apps (5+ repos).

## What

Single source of truth for color, font, radius tokens. Apps install via GitHub URL and `@import`.

## Don'ts

- NEVER change token values without checking visual impact across ALL consuming apps
- NEVER add app-specific styles — this package is tokens only
- NEVER remove tokens — apps depend on them. Deprecate with comments first.
- Don't add JS/TS — CSS-only package

## Consumers

- marusho-dashboard-svelte (bun, dark mode)
- instagram-analytics-2 (bun, dark mode)
- marusho-portal (bun, dark mode)
- magriculture-dashboard (pnpm, light only)
- design-manager (bun, light only)

## Verification Loop

After changing tokens:
1. Commit + push to this repo
2. In ONE consumer app: `bun install --force @marusho/design-tokens && bun run build`
3. Visually verify no regression
4. Repeat for remaining apps or notify team

## Self-Improvement

After every correction, update this file with a rule to prevent repeating it.
