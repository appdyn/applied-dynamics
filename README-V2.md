# Applied Dynamics V2 Visual Refinement

This package is a drop-in replacement for the UI portion of the working Wix Headless Astro project.

## V2 changes
- Animated particle/data-stream homepage hero.
- More balanced homepage headline and pillar spacing.
- Rebuilt internal hero system with dark technology/network visuals instead of the flat gray placeholder treatment.
- Page-specific hero variations for Capabilities, Solutions, Industries, Insights, About, Careers, and Contact.
- Refined global card radius, hover depth, button treatment, and spacing.
- Existing content, routes, segmented-E logo, and Wix integration are preserved.

## Safe install
Commit or back up your current version first. Then copy this package's `src/` over your project's existing `src/`.

Do NOT replace your Wix-generated:
- package.json
- package-lock.json
- astro.config.mjs
- wix.config.json
- tsconfig.json
- node_modules

Then run:

```bash
npm run dev
```

The old `public/images/hero-*.jpg` files are no longer needed by the V2 PageHero, although leaving them in `public/images` is harmless.

The Contact form remains presentation-only until it is wired to Wix Forms/CRM or another backend. The current Insights filters remain presentation-only in this package; CMS/filter wiring can be done after the V2 visual system is approved.
