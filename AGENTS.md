# Project guide

## Overview

This repository contains **Din lokale diætist**, a responsive Danish website for Julie Spanggaard Zielke, an udkørende klinisk diætist near Viborg. It remains under construction with user-supplied services, prices, name, telephone and email; complete business terms are pending. GitHub Pages hosts the static files; `CNAME` contains the custom domain `dinlokalediaetist.dk`.

## Technology

- Use plain HTML, CSS, and vanilla JavaScript.
- No JavaScript framework, bundler, package manager, or build step is required.
- Keep the site publishable directly from the repository root.
- Add JavaScript only when an interaction needs it. Prefer semantic HTML and CSS for content, layout, and simple interactions.

## Files

- `index.html`: page metadata and Danish content, including navigation, hero, services, approach, pricing, contact section, and footer.
- `tilskud-og-forsikring.html`: general subsidy and insurance information, linking to the official provider.
- `handelsbetingelser.html`: preliminary cancellation and travel details; complete terms are pending.
- `styles.css`: shared design tokens, layout, component styles, and responsive rules.
- `images/frokost.png`: hero food photograph.
- `images/raavarer.png`: retained ingredients photograph, currently unused.
- `images/diaetist-portraet.png`: user-supplied portrait in the “Om mig” section, with responsive CSS cropping.
- `images/jylland-kort.svg`: retained earlier map, currently unused. The active OpenStreetMap tile grid and 15 km circle are in `index.html` and styled in `styles.css`.
- `CNAME`: GitHub Pages custom domain configuration.
- `.nojekyll`: disables Jekyll processing for static hosting.
- `README.md`: preview instructions, launch notes, and original image prompts.
- `AGENTS.md`: project structure and guidance for future changes.

There is currently no JavaScript file. If needed, add a descriptive `.js` file and load it with `defer` or `type="module"` from `index.html`.

## Design and components

- Keep visitor-facing copy in Danish, including accessible labels and alt text.
- Follow the existing warm green palette, serif headings, generous spacing, and food photography. Reuse the CSS custom properties in `:root`.
- Build reusable components with semantic HTML and clearly named CSS classes. Existing patterns include `.button`, `.service`, and `.price-card`.
- For interactive components, use small vanilla JavaScript functions or native Web Components when useful. Avoid adding a framework or UI dependency without a user request.
- Keep essential content and navigation usable without JavaScript.
- Preserve keyboard access, visible focus indicators, the skip link, meaningful headings, image descriptions, and reduced-motion support.
- Check responsive behavior when adding or modifying components.

## Development and preview

Open `index.html` in a browser for a basic preview. For automatic browser updates when files are saved, use an editor's static live-preview server with live reload enabled. Live reload is a development convenience, not a site dependency, and is not configured by this repository.

If JavaScript modules or fetch requests are added, preview through a local HTTP server rather than opening a `file://` URL. GitHub Pages publishes the files as static assets; local saves do not automatically publish the live website.

## Verification

There is no automated test suite or build command. Use checks appropriate to the change:

- Preview layout changes at both narrow mobile and desktop widths.
- Check navigation anchors, contact links, and any new interactions.
- Verify image loading and inspect the browser console when changing JavaScript.
- Check keyboard navigation and visible focus for interactive changes.
- Keep asset paths relative so the site works on a GitHub Pages subpath.
- Review `git diff` for unrelated edits before finishing.

## Content and maintenance

- The user explicitly requested OpenStreetMap for the general service-area map. Use standard browser tile requests with visible attribution and caching; never send a private address or use geolocation.
- The user’s home address is secret. Do not include it, identifying home details, address markers, or coordinate links. Do not label the service-area center as a home or clinic. Keep location data local unless the user explicitly authorizes an external lookup.

- Keep the placeholder notices and `noindex, nofollow` metadata until the user requests launch with real content.
- Do not invent business credentials, testimonials, contact details, services, prices, or health claims. Current name, phone, email, services, biography and prices are user-supplied.
- The map circle is 15 km within a 42 km-wide map view (about 71.43% of the image width), using OpenStreetMap zoom 11 for smaller-town labels. Use transparent town labels without white boxes and omit the map header. Supplemental label coordinates are documented in README; keep them aligned with the map projection. The travel surcharge starts after 15 km, at 10 kr. per km beyond that threshold. Keep the threshold consistent across the contact section and terms. Do not restore the visible map caption removed at the user’s request. Follow-ups are 35 minutes; the start package includes the first consultation plus three follow-ups.
- Keep shared navigation and footer consistent across all three HTML pages. All internal links and assets must remain relative.
- Preserve `CNAME` and `.nojekyll` when editing the site.
- Update this guide and `README.md` whenever the file structure, preview process, or deployment approach changes. Documentation updates are manual.
