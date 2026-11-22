# Cloud Runner

A promotional website for the original dystopian sci-fi film *Cloud Runner*

"In a world of floating industrial cities, five teenage tech-scavengers known as the Cloud Runners race to reach a legendary generator city to restore power to their region—hunted across the skies by Caspian, ruthless heir to the White City, a colossal spaceship city that roams the regions siphoning energy from powerless floating islands, until his peacekeeping sister, Silver, teams up with the crew's young leader to try and stop him and bring unity between their worlds."

## User Stories

1. **Cinematic Hero Header (#1)**
   * *User Story:* As a site visitor, I want a full-viewport cinematic hero header when I land on the page, so that I am immediately immersed in the dystopian atmosphere of *Cloud Runner* and can access key calls to action.
   * *Acceptance Criteria:*
     * The hero section spans the full viewport height (`100vh`).
     * Displays a muted video loop with a dark gradient overlay.
     * Features centered title typography (*Cloud Runner*), logline, and a primary CTA button styled with Bootstrap.
     * Transparent navbar is fixed/positioned at the top with working anchor links.

2. **Film Details & Synopsis Grid (#2)**
   * *User Story:* As a film enthusiast, I want to view the official movie poster alongside a clear synopsis and full cast/crew details, so that I can understand the plot and background of the film.
   * *Acceptance Criteria:*
     * Responsive 3-column layout utilising the Bootstrap grid system (`row`, `col-lg-4`).
     * Column 1 displays the 2:3 aspect ratio movie poster with responsive image scaling (`img-fluid`).
     * Column 2 contains the editorial film synopsis and release statement.
     * Column 3 lists structured metadata including starring cast, director, screenplay, and production credits.

3. **Video Teaser & Media Banner (#3)**
   * *User Story:* As an explorer of the site, I want to see a cinematic teaser video section directly below the synopsis, so that I can preview official footage and engage with the visual media.
   * *Acceptance Criteria:*
     * Full-width container section positioned below the main synopsis details.
     * Includes a centred play icon/button element and clear editorial text overlay.

4. **Responsive Multi-Page Navigation (#4)**
   * *User Story:* As a user on any device (mobile or desktop), I want intuitive navigation across all pages (`index.html`, `gallery.html`, `updates.html`), so that I can browse the site quickly without layout breakage.
   * *Acceptance Criteria:*
     * Navbar collapses into a responsive mobile menu on smaller screens using Bootstrap 5 toggle components.
     * All internal links correctly connect the home page, gallery page, and updates page.
     * Floating "Jump to top" button provides fast navigation on long-scrolling mobile views.

5. **Early-Access Contact & Newsletter Form (#5)**
   * *User Story:* As an engaged visitor, I want to submit my email address via a clean early-access sign-up form, so that I can receive release updates and alerts for *Cloud Runner*.
   * *Acceptance Criteria:*
     * Dedicated form inputs styled using Bootstrap form components (`form-control`, `form-label`).
     * Built-in HTML5 input validation for email fields.
     * Success state or redirection feedback when the form is submitted.

6. **Immersive World & Character Gallery (#6)**
   * *User Story:* As a site visitor exploring the *Cloud Runner* world page, I want an immersive top hero section followed by horizontal image galleries for film scenes and character portraits, so that I can explore the visual lore and characters without clutter.
   * *Acceptance Criteria:*
     * Dedicated `gallery.html` page featuring a cinematic top hero banner matching the site's design language.
     * Scene Gallery: A horizontal scrolling card carousel utilizing CSS scroll-snap and flexbox layout with forward and previous navigation arrows to browse film stills.
     * Character Portraits Gallery: A separate horizontal image gallery showcasing key character visuals and lore cards.
     * Fully responsive design ensuring smooth touch-scrolling and clean alignment on mobile and desktop viewports.

## Design

### Color Scheme

The visual palette for *Cloud Runner* pairs deep atmospheric charcoal-slate backgrounds with crisp off-white typography and a cool teal-blue interactive accent[cite: 13]:

| Hex Value | Role & Usage |
| :--- | :--- |
| `#101416` | Primary page/body background (`body`), gallery header background (`.gallery-navbar-header`), and hero CTA hover text (`.hero-content .btn:hover`)[cite: 13] |
| `#101214` | Form inputs and select menus (`.updates-form input`, `.updates-form select`), gallery cards (`.gallery-card`), and trailer container background (`.trailer-section .ratio`)[cite: 13] |
| `#181b1f` | Film details/synopsis section background (`.film-details`) and updates page main container (`.updates-main`)[cite: 13] |
| `#080c0e` | Site footer background (`.site-footer`)[cite: 13] |
| `#f0f0ec` | Primary off-white text and borders across the hero, synopsis, cast/crew credits, forms, gallery, carousel, footer, and confirmation views[cite: 13] |
| `#ffffff` | Pure white hover, focus, and active states for navigation links (`.cloud-nav-link`), brand text (`.cloud-home`), and cinematic banner headings[cite: 13] |
| `#82bdca` | Atmospheric teal-blue accent for the game page heading and CTA (`.game-hero`), plus default, hover, focus, and mobile collapsed navigation link states[cite: 13] |

* **Overlays & Contrast:** Translucent dark gradient overlays derived from the base dark palette sit behind hero banners, carousel frames, and video sections so light typography (`#f0f0ec` / `#ffffff`) remains legible across desktop and mobile viewports.

### Typography

* **Primary Font (`Inter`):** Imported via Google Fonts and applied consistently across body copy, navigation, synopses, credits, cards, and form controls, paired with clean system sans-serif fallbacks (`sans-serif`) so text renders immediately without layout shift.
* **Display & Editorial Hierarchy:** Headings, theatrical release banners, and interactive CTAs use uppercase styling, deliberate font weights, and wide letter-spacing (`letter-spacing`) to create a sharp cinematic title-card aesthetic without relying on heavy external display font files.

## Features

### Existing Features

* **Responsive Navigation Bar (`.cloud-navbar`):** Fixed/transparent header on hero pages and solid dark header on subpages featuring the *Cloud Runner* brand link, accessible active-page indicators (`aria-current="page"`), high-contrast hover/focus states, and a collapsible mobile menu with a custom dark backdrop (`max-width: 767.98px`) for clear legibility over video and imagery.
* **Home Page (`index.html`):**
  * **Full-Viewport Hero Section:** Autoplaying, muted, looping atmospheric background video paired with dark gradient overlays, the film title, release window (*In Cinemas Fall 2027*), and primary call-to-action buttons (*Watch Teaser* / *Explore Gallery*).
  * **Film Details, Poster & Credits Grid:** Three-column responsive layout presenting the official *Cloud Runner* theatrical poster, official synopsis, cast and crew billing (directed by Henrik Lindqvist, starring Callum Reid, Noah Gallagher, Darius Okafor, Leo Castellanos, Tomasz Novak, and Julian Thorne), and release metadata.
  * **Cinematic Teaser & Trailer Showcase:** Full-bleed atmospheric banner and responsive 16:9 trailer section (`ratio-16x9`) featuring custom preview video and score audio.
* **Character & World Gallery (`gallery.html`):**
  * **Gallery Hero Banner:** Full-width visual header introducing the divided world of the floating islands and the upper capital.
  * **Interactive Character Showcase:** Responsive desktop carousel with custom slide indicators and controls paired with a dedicated mobile vertical card layout (`.gallery-mobile-list`), profiling the five Cloud Runners, Caspian Vane, and Silver using optimized WebP portraits.
* **Early-Access Updates Sign-Up (`updates.html`):**
  * **Interactive Subscription Form:** Clean dark-themed form collecting visitor name, email address, preferred sector/region, and genre/interest selection, using native HTML5 validation alongside custom validation feedback to prevent incomplete submissions before redirecting to the confirmation view.
* **Subscription Confirmation (`thank-you.html`):**
  * **Dedicated Confirmation State:** Atmospheric confirmation screen acknowledging early-access registration and providing a direct return path to the main site.
* **Game Teaser Page (`game.html`):**
  * **Interactive Experience Preview:** Dedicated promotional preview page featuring full-bleed background video, `#82bdca` teal-blue accent styling, and teaser copy introducing the *Cloud Runner* companion experience.
* **Site Footer (`.site-footer`):** Consistent dark footer (`#080c0e`) across all pages with copyright details, studio/production credits, and social media links.

## Technologies & Tools Used

### Languages

* **HTML5:** Semantic structure and content across all project pages.
* **CSS3:** Custom styling, responsive layouts, Flexbox, CSS Grid, variables, and media queries.
* **JavaScript (ES6):** Client-side form validation logic on the updates page.

### Frameworks & Libraries

* **Bootstrap 5:** Rapid responsive grid system, utility classes, navigation components, and modal/carousel framework.
* **Google Fonts:** Sourcing and implementation of the project typography (`Inter` with `sans-serif` fallback).
* **Font Awesome:** Scalable vector icons used in navigation links, buttons, and the footer.

### Programs & Services

* **VS Code:** Primary Integrated Development Environment (IDE) for writing code.
* **Git:** Version control system used to track changes and commit code.
* **GitHub:** Cloud-based hosting platform for Git repositories, issue tracking, and project management.
* **GitHub Pages:** Hosting service used to deploy the live version of the website.
* **Google Flow AI:** Used for generating background video and teaser audio assets.
* **Google Chrome DevTools:** Browser-based suite used extensively for debugging, testing responsiveness, and Lighthouse auditing.
* **W3C Markup Validation Service & CSS Validation Service:** Used for validating HTML and CSS code quality and compliance.

## Deployment

The *Cloud Runner* promotional website is deployed and hosted using **GitHub Pages** directly from the `main` branch of the GitHub repository.

### Deploying to GitHub Pages

1. Push all committed project files (`index.html`, `gallery.html`, `updates.html`, `thank-you.html`, `game.html`, `assets/`, and `README.md`) to the `main` branch on GitHub (`https://github.com/raf-src/cloud-runner-film-promo`).
2. Open the repository on **GitHub** and navigate to **Settings** > **Pages** (under the *Code and automation* section).
3. Under **Build and deployment** > **Source**, select **Deploy from a branch**.
4. Set **Branch** to **`main`** and the folder to **`/ (root)`**, then click **Save**.
5. Wait a minute or two for GitHub Actions / Pages to build and publish the site; the live URL will appear on the **Pages** settings screen (`https://raf-src.github.io/cloud-runner-film-promo/`).

### Updating the Live Site

Because the project uses static HTML5, CSS3, Bootstrap 5, and vanilla JavaScript with relative asset paths (`assets/...`), pushing new commits to `main` automatically triggers a GitHub Pages rebuild so updates go live without extra server configuration.

## Lighthouse Testing & Performance Audits (Desktop & Mobile)

Audits were run in Chrome DevTools (Incognito) against the live GitHub Pages deployment for both **Desktop** and **Mobile** viewports, comparing the baseline run (`2026-11-20`) against the latest run (`2026-11-22`)[cite: 1, 2, 10, 11, 14, 15, 16, 17].

### Key Optimisations Applied Between Runs
* **Image Format & Compression:** Converted key assets to `.webp` and optimised file sizes to speed up Largest Contentful Paint (LCP).
* **Above-the-Fold Priority:** Added `fetchpriority="high"` to primary hero/portrait assets, kept `loading="lazy"` on below-the-fold portraits, and preloaded the gallery header background image (`<link rel="preload" as="image" ... fetchpriority="high">`) in `gallery.html`.
* **Viewport & Background Scaling:** Updated hero containers (including `.updates-hero` and `.updates-hero-thank-you`) to use `100svh`, `min-height: 500px`, and `background-size: cover` so desktop and mobile framing stay consistent without awkward cropping or overflow[cite: 16].

### First Test vs. Latest Test Results

| Page | Viewport | First Test (`2026-11-20`)<br>Perf / Acc / BP / SEO | Latest Test (`2026-11-22`)<br>Perf / Acc / BP / SEO | Perf Delta |
| :--- | :--- | :---: | :---: | :---: |
| `index.html` | Desktop | 95 / 100 / — / 100 | **99 / 100 / 96 / 100**[cite: 1] | +4[cite: 1] |
| `index.html` | Mobile | 94 / 100 / — / 100 | **96 / 100 / 96 / 100**[cite: 2] | +2[cite: 2] |
| `gallery.html` | Desktop | 80 / 100 / — / 100 | **99 / 100 / 100 / 100**[cite: 10] | +19[cite: 10] |
| `gallery.html` | Mobile | 73 / 100 / — / 100 | **89 / 100 / 100 / 100**[cite: 11] | +16[cite: 11] |
| `updates.html` | Desktop | 61 / 100 / — / 100 | **100 / 100 / 100 / 100**[cite: 14] | +39[cite: 14] |
| `updates.html` | Mobile | 98 / 100 / — / 100 | **97 / 100 / 100 / 100**[cite: 15] | -1[cite: 15] |
| `music.html` | Desktop | *Not recorded in first set* | **100 / 100 / 100 / 100**[cite: 16] | — |
| `music.html` | Mobile | *Not recorded in first set* | **97 / 100 / 100 / 100**[cite: 17] | — |
| `thank-you.html` | Desktop | 85 / 98 / 100 / 100[cite: 17] | **100 / 98 / 100 / 100**[cite: 18] | +15[cite: 17, 18] |
| `thank-you.html` | Mobile | 97 / 98 / 100 / 100[cite: 17] | **97 / 98 / 100 / 100**[cite: 12, 15] | 0[cite: 15, 17] |

*(Note: `game.html` was included in the `2026-11-20` baseline set at **100 / 100 / 100 / 100** on Desktop and **97 / 100 / 100 / 100** on Mobile; `music.html` was audited in the latest pass[cite: 16, 17].)*

## Code Validation (W3C HTML & CSS)

All HTML pages and custom CSS were validated on `2026-11-22` using the W3C Markup Validation Service (`validator.w3.org`) and the W3C CSS Validation Service (`jigsaw.w3.org/css-validator/`) via direct input[cite: 6, 7, 8, 9, 10, 11].

### HTML Validation Results

| File | Validator | Result |
| :--- | :--- | :--- |
| `index.html` | W3C Markup Validation Service | Passed — 0 errors, 0 warnings[cite: 6] |
| `gallery.html` | W3C Markup Validation Service | Passed — 0 errors, 0 warnings[cite: 7] |
| `updates.html` | W3C Markup Validation Service | Passed — 0 errors, 0 warnings[cite: 8] |
| `thank-you.html` | W3C Markup Validation Service | Passed — 0 errors, 0 warnings[cite: 9] |
| `music.html` | W3C Markup Validation Service | Passed — 0 errors, 0 warnings[cite: 10] |

### CSS Validation Results

| File | Validator | Result |
| :--- | :--- | :--- |
| `assets/css/styles.css` | W3C CSS Validation Service | Passed — 0 errors, 0 warnings[cite: 9, 10, 11] |

## Credits

### Concept, Story & Development

* **Original Concept & World-Building:** Created for *Cloud Runner*, including the setting, character dynamics, and promotional site copy.
* **Web Development & Design Implementation:** Built with HTML5, CSS3, Bootstrap 5, and JavaScript, with styling refinements and accessibility contrast updates developed in VS Code.

### Media & Visual Assets

* **AI Video & Imagery:** Generated with **Google Flow** and refined/composited in **Adobe Illustrator** and **Adobe Photoshop** (including WebP optimization for web performance and the custom color palette swatch).
* **Audio & Score Preview:** Generated with **Flow Music** for the *Cloud Runner* teaser/trailer experience.

### Frameworks, Libraries & Acknowledgments

* **Bootstrap 5, Font Awesome & Google Fonts:** Used for responsive layout structure, icons, and `Inter` typography.
* **Mentorship & Feedback:** Thanks to bootcamp tutors and peers at WAES and Code Institute for guidance, feedback, and code walkthroughs during development.

## Concept Ownership & Copyright

* **Original Concept & IP:** *Cloud Runner*—including its premise, floating-island world-building, and characters (including the five teenage scavengers led by **Rowan Cole**, his younger brother **Toby Cole**, their adopted brother **Jules Mercer** and the 'Gemini' twin brothers **Marek Hale** and **Kieran Hale**, alongside **Silver Vane** and **Caspian Vane**), narrative copy, and promotional website implementation—is an original concept created by **Raf Joseph (`raf-src`)**.
* **Copyright Notice:** © 2026 Raf Joseph. All rights reserved. Original written narrative, character descriptions, site copy, and custom code in this repository may not be reproduced, redistributed, or adapted into derivative works without permission.
* **Third-Party & Generated Assets:** AI-assisted visuals and audio generated via Google Flow / Flow Music remain subject to their respective tool terms, while Bootstrap 5, Font Awesome, and Google Fonts remain under their respective licenses.
