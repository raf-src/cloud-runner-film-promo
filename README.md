# Cloud Runner

A promotional website for the original dystopian sci-fi film *Cloud Runner*

"In a world of floating industrial cities, five teenage tech-scavengers known as the Cloud Runners race to reach a legendary generator city to restore power to their region—hunted across the skies by Caspian, ruthless heir to the White City, a colossal spaceship city that roams the regions siphoning energy from powerless floating islands, until his peacekeeping sister, Silver, teams up with the crew's young leader to try and stop him and bring unity between their worlds."

### User Stories

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
