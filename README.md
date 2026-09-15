# Yaman Obiedat — Portfolio

A responsive, charcoal-and-ivory portfolio for AI systems engineering. Built from the approved design concept using semantic HTML, CSS, and dependency-free browser JavaScript.

## Run locally

```sh
python3 -m http.server 4317 --bind 127.0.0.1 --directory dist
```

Open http://127.0.0.1:4317. No package installation or compilation is required.

## Structure

- `dist/index.html`: page structure, profile, navigation, contact, and metadata.
- `dist/styles.css`: responsive layout, typography, colors, and transitions.
- `dist/app.js`: project content, accessible project dialogs, scroll-snap carousel, and original canvas particle sculpture.
- `dist/assets/project-art.png`: generated conceptual project-cover artwork.
- `.openai/hosting.json`: private Sites project and static output configuration.

## Content and assets

The 12 project summaries and contact information are drawn from the existing `profile-redesign/README.md` and `profile-redesign/jade-profile/README.md` supplied in the workspace. Project descriptions preserve the distinction between individual contributions, team projects, system overviews, and course work. RegTech V3 authorship is not asserted; the public link is identified as an earlier version. No private code or internal reports are included.

Cover artwork is conceptual, not product screenshots. Generated with the built-in image-generation tool using this prompt: “Gallery-quality minimal 3D editorial terrain with charcoal folded planes, misty sage flowing metal, softly lit pale stone sphere; wide 3:2 composition suitable for three cropped portfolio views; charcoal/ivory/sage palette; no text, UI, logos, watermark, or border.”

The particle sculpture and carousel are original implementations for the approved concept. They are **not** the exact ThreeUI SylvaHero, PredictiveArcCanvas, or CharacterCarousel components: the registered source files were not available. Exact integration requires those original source files and checksum verification.

DM Sans and Manrope are loaded from Google Fonts, with system-font fallbacks. The site otherwise needs no external runtime. Motion respects reduced-motion preferences, can be paused, and stops when offscreen or the tab is hidden. Native modal dialogs support Escape, focus trapping, and focus restoration.

## Validation

- JavaScript syntax verified with `node --check dist/app.js`.
- Browser checked at desktop and 390px mobile width.
- Project dialog opening and Escape dismissal verified.
- Carousel advance and position indicator verified.
- Background pause/play state verified.
- All six cover images loaded; no horizontal page overflow at 390px.
- Email, LinkedIn, and GitHub destinations verified against the supplied profile content.

## Edit

Update the `projects` array in `dist/app.js` to change project descriptions or repository links. Update `dist/index.html` for bio and contact details. Replace the conceptual covers with real screenshots when available.

## GitHub Pages deployment

The workflow in `.github/workflows/deploy-pages.yml` publishes only `dist/` to GitHub Pages when website files are pushed to `codex/portfolio`. It also supports manual runs. It uses GitHub's built-in token and requires no stored deployment secret.

The repository is public with the owner's approval. GitHub Pages uses GitHub Actions as its publishing source. Updates to website files on `codex/portfolio` deploy automatically. The existing private Sites deployment is independent and remains available.
