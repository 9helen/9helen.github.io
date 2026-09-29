# Project conventions

## Project overview

This is Helen Yin's personal portfolio website. It is a static, multi-page site published with GitHub Pages from the main branch of 9helen/9helen.github.io.

## Tech stack

- Semantic HTML5 pages; no frontend framework or component build step.
- One shared stylesheet, styles.css, using CSS custom properties and responsive media queries.
- One small vanilla JavaScript file, script.js, for the responsive navigation menu and current-year footer.
- Google Fonts (DM Sans and Manrope) loaded by CSS from Google Fonts.
- Decorative background video and gradient image loaded from the GetLayers public asset host.
- Resume content is served as a PDF and embedded on resume.html.
- No package manager, bundler, application server, or test suite is configured.

## Files and pages

- index.html — home page and links to the portfolio sections.
- experience.html — work experience and technologies.
- education.html — education entries, including the University of Toronto (St. George) non-degree program.
- activities.html — volunteer experience and activities.
- resume.html — resume PDF viewer and download link.
- styles.css — shared visual system, layout, components, and responsive styles.
- script.js — mobile menu behavior and dynamic footer year.
- Helen_Yin_Resume.pdf — PDF filename expected by the resume page.

## Run locally

There is no build step. From the project directory, start Python's static file server:

```sh
python3 -m http.server 8000
```

Open http://localhost:8000 in a browser. Stop the server with Ctrl+C.

Opening the HTML files directly also works for basic review, but use the local server to check navigation and PDF links in a browser.

## Page and content conventions

- Keep the site framework-free unless the project requirements change.
- Use lowercase, hyphen-free filenames for pages, and link pages with relative paths such as education.html.
- Preserve semantic landmarks (header, nav, main, section, article, and footer) and descriptive page titles and meta descriptions.
- Keep the shared header, navigation, ambient background, footer, and script.js include consistent on every page.
- Mark the current navigation link with both .active and aria-current="page".
- Use the existing shared classes for page structure and content: .page-main, .page-title, .page-intro, .content-section, .section-heading, .placeholder-entry, .entry-meta, and .secondary-entry.
- Keep repeated entries evenly spaced and follow the established typography, capitalization, date, and location patterns on sibling pages.
- Use the CSS variables in :root for shared colors and fonts. Put shared styling in styles.css rather than adding page-specific inline styles.
- Preserve responsive behavior at the existing 800px and 620px breakpoints and the prefers-reduced-motion handling.
- Keep interactive controls accessible: preserve button labels, navigation labels, aria-expanded, and aria-current state.
- The home page and Resume page use Helen_Yin_Resume.pdf; update that file when publishing a replacement resume so the download and embedded viewer stay in sync.

## Preview and publishing

- GitHub Pages serves the root-level static files from the repository's main branch at https://9helen.github.io/.
- Keep deployable HTML, CSS, JavaScript, and linked assets at the repository root or at paths referenced by the pages.
- Commit updates to the main branch to publish through GitHub Pages. Allow a short delay for the deployed site to refresh.
- Check the changed page at desktop and narrow viewport widths after layout changes; verify the navigation links and, for resume changes, both PDF viewing and downloading.

## Current content notes

- The Education page lists University of Toronto (St. George), University of British Columbia, and Technische Universität Darmstadt.
- The project working folder may contain both Helen_Yin_Resume.pdf and Helen_Yin_Resume_Updated.pdf. The page link targets Helen_Yin_Resume.pdf; use the updated file to replace that target when a resume PDF upload is requested.
