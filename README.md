# Applied Dynamics UI replacement package

## Install

This contains only website UI images, Astro components, layouts, pages, and CSS. It contains no Wix-generated package, build, integration, or configuration files.

1. Back up existing `src` files before replacement.
2. Copy the contents of `public/images/` into your project's `public/images/`.
3. Copy `src/components/ApprovedHero.astro` and `src/components/ServiceCard.astro` into `src/components/`.
4. Copy `src/layouts/AppliedLayout.astro` into `src/layouts/` and `src/styles/applied-dynamics.css` into `src/styles/`.
5. Replace `src/pages/index.astro`, `capabilities.astro`, `solutions.astro`, `industries.astro`, `insights.astro`, `about.astro`, `careers.astro`, and `contact.astro`. If your project uses route folders, replace the corresponding `index.astro` routes instead; do not keep duplicate routes. These pages use the new layout directly. Preserve any Wix-required application wrappers, scripts, and existing form integration when merging into your project.
6. Run your existing project's build and preview commands. No existing project files were available here, so Wix integration and a real Astro build have not been verified.

## Visual approach and resolution limits

The supplied source is a single 1536 × 1024 PNG showing all eight pages. Individual page headers are only 308–498 pixels wide. Every WebP is a pixel-exact lossless crop: no AI redraw, filtering, resampling, sharpening, or invented detail. All exports were compared pixel for pixel with their original crops.

The header images retain the approved text and imagery together to prevent composition drift. Their headings and descriptions also exist as screen-reader-accessible HTML. Home has keyboard-accessible clickable hotspots over the two pictured calls to action. Cards, navigation, page copy, and the contact form are HTML. White-background icons and the original logo are extracted directly. Arial/Helvetica are a font-feel approximation for HTML because no font files or font identity were supplied; the artwork retains its original typography.

The layout uses a standard 1280px desktop container and a 700px mobile breakpoint, with single-column mobile content. Desktop/mobile filenames are separate, but currently contain identical native-resolution header crops: the source has no separate approved mobile composition. Browser enlargement WILL soften these small images; lossless encoding cannot solve that. This is a fidelity-first implementation draft, not a claim of sharp high-resolution production imagery. To finish that requirement, replace headers with original high-resolution exports (ideally 2560px desktop and 1080px mobile) and supply the original logo/vector assets and fonts. Do not upscale these crops to those widths and call them high-resolution. When replacing differently composed hero art, update dimensions and Home hotspot coordinates.

## Page-to-WebP mapping

Images are requested as `/images/name.webp`, never `/public/images/name.webp`.

| Page | WebP asset | Native pixels |
| --- | --- | --- |
| Home | `home-hero-desktop.webp` | 496 × 465 |
| Home | `home-hero-mobile.webp` | 496 × 465 |
| Capabilities | `capabilities-hero-desktop.webp` | 336 × 135 |
| Capabilities | `capabilities-hero-mobile.webp` | 336 × 135 |
| Solutions | `solutions-hero-desktop.webp` | 341 × 146 |
| Solutions | `solutions-hero-mobile.webp` | 341 × 146 |
| Industries | `industries-hero-desktop.webp` | 308 × 115 |
| Industries | `industries-hero-mobile.webp` | 308 × 115 |
| Insights | `insights-hero-desktop.webp` | 498 × 86 |
| Insights | `insights-hero-mobile.webp` | 498 × 86 |
| About | `about-hero-desktop.webp` | 333 × 123 |
| About | `about-hero-mobile.webp` | 333 × 123 |
| Careers | `careers-hero-desktop.webp` | 337 × 113 |
| Careers | `careers-hero-mobile.webp` | 337 × 113 |
| Contact | `contact-hero-desktop.webp` | 313 × 124 |
| Contact | `contact-hero-mobile.webp` | 313 × 124 |

`asset-manifest.json` lists all image dimensions and exact source crop coordinates. The remaining images are the three Capabilities illustrations, four Industries images, six Insights thumbnails, extracted icons, and the original Applied Dynamics logo. Home only contains the hero, as labeled in the supplied design.

## Connections still required

- Main navigation, Home calls to action, and Insights category filtering work.
- Learn More, article arrows, About team, and View Details controls retain their labels but are disabled because no destination pages or URLs were supplied. Supply real routes to activate them; this package invents no detail pages.
- The contact form is UI only. Submitting displays an explicit “Message not sent” status; no data is transmitted. Replace the submit handler with the existing Wix form integration before launch.
- Contact details and dates are transcribed from the composite, including its 555 phone number. Confirm these design values before publishing.
- Some source copy is very small. Text has been transcribed as closely as legible; exact source text files are needed to certify every word.
- The HTML header consistently exposes all eight requested page routes. The source navigation varies between panels; no additional content sections or footer were invented.

## Verification

All exported WebPs are decoded and checked pixel-for-pixel against their source crops. All static image references and eight page files are checked. No Astro runtime or existing Wix project was present, so build, browser interaction, and deployed visual fidelity are not verified. This package does not deploy or alter Wix configuration.




# Applied Dynamics Astro UI Pack

Copy the included `src/` folders into a fresh Wix Headless Astro scaffold.

Do not replace Wix-generated files such as `package.json`, `package-lock.json`, `astro.config.mjs`, `wix.config.json`, or `tsconfig.json`.

Routes included:
- `/`
- `/capabilities`
- `/solutions`
- `/industries`
- `/insights`
- `/about`
- `/careers`
- `/contact`

Optional images can be placed in `public/images/` using these names:
- hero-capabilities.jpg
- hero-solutions.jpg
- hero-industries.jpg
- hero-insights.jpg
- hero-about.jpg
- hero-careers.jpg
- hero-contact.jpg

Notes:
- Insights filters are visual-only in this starter.
- Contact form is visual-only until wired to Wix Forms/CRM or another backend.


Applied Dynamics V3 replacement package

Copy/replace these files in your project:

public/images/
  home-hero.jpg
  capabilities-hero.jpg
  insights-hero.jpg

src/components/
  HomeHero.astro
  PageHero.astro

src/pages/
  capabilities.astro
  insights.astro

What changed:
- Home artwork is confined to the right side instead of being stretched across the entire hero.
- Home capability labels are real HTML rendered over glass cards:
  AI & Agentic Workflows, Cloud Engineering, Cybersecurity, Secure Implementation.
- Hero images were exported at 3840px wide for large/Retina screens.
- Capabilities and Insights use their static hero files through PageHero.astro.
- Insights article thumbnails remain neutral placeholders until real content is published.
- No Wix config, package.json, or dependency files are included.

After replacing the files, run:
npm run dev

