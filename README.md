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

