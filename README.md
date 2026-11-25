**[View the Live Deployed Website on GitHub Pages](https://raf-src.github.io/cloud-runner-film-promo/)**

![Cloud Runner Multi-Device UI](assets/doc-images/cloud-runner-multi-device-ui-image-title.jpeg)

# Cloud Runner — Official Film Promotional Website

A promotional website for the original dystopian sci-fi film *Cloud Runner*.

> *"In a world of floating industrial cities, five teenage tech-scavengers known as the Cloud Runners race to reach a legendary generator city to restore power to their region—hunted across the skies by Caspian, ruthless heir to the White City, a colossal spaceship city that roams the regions siphoning energy from powerless floating islands, until his peacekeeping sister, Silver, teams up with the crew's young leader to try and stop him and bring unity between their worlds."*

## Table of Contents

- [Purpose & User Stories](#purpose--user-stories)
- [Features & User Benefits](#features--user-benefits)
- [Project Planning](#project-planning)
- [Design](#design)
- [Technologies & Tools Used](#technologies--tools-used)
- [Deployment](#deployment)
- [Bugs & Errors](#bugs--errors)
- [Validation](#validation)
- [Credits, Attribution & Ownership](#credits-attribution--ownership)
- [Declaration of Use of AI](#declaration-of-use-of-ai)
- [Future Features](#future-features)
  
## Purpose & User Stories

*Cloud Runner* is a responsive multi-page promotional website built with HTML5, CSS3, and Bootstrap 5 for an original sci-fi film project. It introduces visitors to the story world, showcases key characters and visual teasers, highlights the soundtrack, and provides an updates sign-up flow.

1. **Cinematic Hero Header (#1)**
   - *User Story:* As a site visitor, I want a full-viewport hero header when I land on `index.html` so I am immediately immersed in the atmosphere of *Cloud Runner* and can access key calls to action.
   - *Acceptance Criteria:*
     - Full-viewport hero section (`100vh`) with a muted background video loop, dark gradient overlay, centered title, release window (*In Cinemas Fall 2027*), and primary call-to-action button.
     - Top navigation bar positioned cleanly without blocking the hero focal point.
   - *Tasks Completed:* Built the hero section in `index.html`, styled the overlay and responsive sizing in `assets/css/styles.css`, converted media assets to `.webp`, and verified performance with Lighthouse.

2. **Film Details, Poster & Credits Grid (#2)**
   - *User Story:* As a film enthusiast, I want to view the official movie poster alongside a clear synopsis and cast/crew credits on `index.html` so I understand the plot and production background.
   - *Acceptance Criteria:*
     - Responsive multi-column Bootstrap layout presenting the movie poster, story synopsis, and structured cast/crew credits.
     - Text and images scale cleanly across desktop and mobile viewports.
   - *Tasks Completed:* Structured the poster, synopsis, and cast/crew columns in `index.html`, refined spacing and typography in `assets/css/styles.css`, and checked desktop and mobile page captures.

3. **Video Teaser & Media Showcase (#3)**
   - *User Story:* As a visitor exploring `index.html`, I want a teaser video section so I can preview footage and engage with the visual media.
   - *Acceptance Criteria:*
     - Responsive 16:9 trailer section (`ratio-16x9`) and supporting media framing positioned below the film details.
     - Controls and media render cleanly across screen sizes.
   - *Tasks Completed:* Added and styled the responsive 16:9 trailer section in `index.html` and `assets/css/styles.css`, optimized assets, and validated markup and layout.

4. **Responsive Multi-Page Navigation & Footer (#4)**
   - *User Story:* As a visitor on desktop or mobile, I want consistent navigation and footer links across `index.html`, `gallery.html`, `updates.html`, `music.html`, and `thank-you.html` so I can move smoothly around the site.
   - *Acceptance Criteria:*
     - Shared navigation bar (collapsing to a mobile menu button on smaller screens) and footer across all five pages.
     - All internal links connect the five pages reliably without layout breakage.
   - *Tasks Completed:* Standardized the navbar and `.site-footer` across all five pages, fixed W3C HTML/CSS validation issues, and verified desktop and mobile page views.

5. **Character & World Gallery (#5)**
   - *User Story:* As a visitor exploring `gallery.html`, I want to browse the key characters and their roles across both desktop and mobile screens.
   - *Acceptance Criteria:*
     - Dedicated `gallery.html` page with a visual header and character profiles (Rowan Cole, Toby Cole, Kieran Hale, Marek Hale, Jules Mercer, Silver Vane, and Caspian Vane).
     - Responsive layout that adapts cleanly from desktop to a stacked mobile view without horizontal overflow.
   - *Tasks Completed:* Created the character profiles in `gallery.html`, added the desktop carousel and stacked mobile layout with `16 / 9` framing and font sizing in `assets/css/styles.css`, and converted portraits to `.webp`.

6. **Soundtrack Preview, Updates Sign-Up & Confirmation (#6)**
   - *User Story:* As an engaged fan, I want to explore the *"Skybound"* soundtrack on `music.html`, sign up for release updates on `updates.html`, and see confirmation on `thank-you.html`.
   - *Acceptance Criteria:*
     - Dedicated `music.html` page introducing *"Skybound"* with clear navigation/calls to action.
     - Form on `updates.html` with name, contact, email, optional details, genre selection, and consent controls with validation, routing to `thank-you.html` upon submission.
   - *Tasks Completed:* Built `music.html`, `updates.html`, and `thank-you.html`, updated hero viewport sizing (`100svh`, `min-height: 500px`, `background-size: cover`), and passed W3C and Lighthouse checks across all three pages.

## Features & User Benefits

- **Responsive Multi-Page Navigation (`.cloud-navbar`):** Consistent navigation across `index.html`, `gallery.html`, `updates.html`, `music.html`, and `thank-you.html` with a collapsible mobile menu and clear active/focus states.
- **Home Page (`index.html`):** Full-viewport hero header with background video and CTA, atmospheric banner, three-column poster/synopsis/cast-and-crew grid, and responsive 16:9 trailer showcase.
- **Character & World Gallery (`gallery.html`):** Visual header plus a responsive desktop carousel and mobile stacked card list profiling the *Cloud Runner* cast and characters using optimized `.webp` portraits.
- **Soundtrack Page (`music.html`):** Dedicated showcase highlighting the soundtrack direction and teaser track (*"Skybound"*).
- **Early-Access Updates & Confirmation (`updates.html`, `thank-you.html`):** Subscription form with native HTML5 validation that redirects to a dedicated confirmation page upon submission.
- **Site Footer (`.site-footer`):** Consistent dark footer across all pages with copyright notice, legal/contact links, and social media links.

## Project Planning

Work on *Cloud Runner* was organised using a GitHub Projects board (**Cloud Runner Project Planning Board**), tracking core `must-have` features from planning through to completion.

![Cloud Runner Project Planning Board](assets/doc-images/cloud-runner-github-project-planning-board.jpeg)

- **Tracked scope:** All six `must-have` tasks—covering the cinematic hero header, film details and synopsis grid, video teaser and media banner, responsive multi-page navigation, updates/newsletter form, and character gallery page—were completed and moved to **Done**.

## Design

### Color Scheme

The visual palette pairs deep slate and charcoal-slate backgrounds with off-white/white typography and cool teal-blue accents:

| Hex Value | Role & Usage |
| :--- | :--- |
| `#101416` | Primary page background (`body`), gallery header, and hero CTA hover text |
| `#101214` | Form controls, gallery cards, and trailer container background |
| `#181b1f` | Film details/synopsis section and updates main container background |
| `#080c0e` | Site footer background (`.site-footer`) |
| `#f0f0ec` | Primary off-white text and borders across sections, forms, cards, and footer |
| `#ffffff` | High-contrast hover, focus, and active states for navigation and headings |
| `#82bdca` | Teal-blue accent for highlights and interactive states |

- **Overlays & Contrast:** Dark gradient overlays sit behind hero banners, media frames, and video sections so light text remains legible across desktop and mobile viewports.

### Typography

- **Primary Font (`Inter`):** Imported via Google Fonts with system `sans-serif` fallbacks across body copy, navigation, synopses, credits, cards, and forms.
- **Display Hierarchy:** Uppercase headings, release banners, and CTAs with measured weights and letter-spacing for a cinematic title-card aesthetic.

## Technologies & Tools Used

### Languages & Frameworks
- **HTML5:** Semantic markup across all five pages.
- **CSS3:** Custom styling, responsive layouts, Flexbox, CSS Grid, variables, and media queries.
- **Bootstrap 5:** Responsive grid system, utility classes, navbar, and carousel/ratio components.
- **Google Fonts (`Inter`) & Font Awesome:** Typography and scalable icons.

### Tools & Services
- **VS Code, Git, GitHub & GitHub Pages:** Editor, version control, repository hosting, and static deployment.
- **Google Flow:** Visual teaser/character artwork and video generation.
- **Google Chrome DevTools & W3C Validators:** Responsiveness testing, Lighthouse auditing, and HTML/CSS validation.
- **Custom Favicon:** Scalable SVG browser tab icon generated with Gemini and linked across all five HTML pages.
  
  ![Favicon Asset](assets/doc-images/cloud-runner-favicon.svg)

## Deployment

The website is deployed via **GitHub Pages** from the `main` branch (`https://raf-src.github.io/cloud-runner-film-promo/`).

1. Commit and push all project files (`index.html`, `gallery.html`, `updates.html`, `music.html`, `thank-you.html`, `assets/`, and `README.md`) to `main` on GitHub (`https://github.com/raf-src/cloud-runner-film-promo`).
2. In the GitHub repository, open **Settings** > **Pages**.
3. Under **Build and deployment** > **Source**, select **Deploy from a branch**, choose **`main`** and **`/ (root)`**, and save.
4. Pushing subsequent commits to `main` automatically triggers a GitHub Pages rebuild.

## Bugs & Errors

### Resolved Bugs & Technical Fixes

| Issue | Page / File | Fix Applied |
| :--- | :--- | :--- |
| **W3C HTML Validation Errors** | `index.html`, `gallery.html`, `updates.html`, `music.html`, `thank-you.html` | Removed trailing slashes on void elements (`<meta>`, `<link>`, `<img>`) and fixed invalid `aria-label` usage on non-interactive `<div>` elements so all five pages pass with `0` errors and `0` warnings. |
| **W3C CSS Syntax & Cascade Cleanup** | `assets/css/styles.css` | Fixed `border-width` syntax, removed unused/duplicate rules, consolidated media queries, and structured styles cleanly so the stylesheet passes with `0` errors and `0` warnings. |
| **Large Image Payloads & LCP** | All pages, `assets/images/` | Converted heavy images to `.webp`, applied `loading="lazy"` where appropriate, and added `fetchpriority="high"` / preloading on key hero/header assets. |
| **Mobile Gallery Layout** | `gallery.html`, `assets/css/styles.css` | Added a dedicated stacked mobile layout below the desktop carousel breakpoint and tuned mobile typography and `16 / 9` image framing to prevent horizontal overflow. |
| **Footer Alignment** | All pages, `assets/css/styles.css` | Standardized footer spacing and flex wrapping across desktop and mobile viewports. |

### Known Issues
- None.

## Validation

### Desktop & Mobile Page Views

Desktop and mobile captures across all five pages of the deployed site.

- **Home (`index.html`)**
  ![Home Desktop View](assets/doc-images/cloud-runner-page-index-desktop.png)
  ![Home Mobile View](assets/doc-images/cloud-runner-page-index-mobile.png)

- **Gallery (`gallery.html`)**
  ![Gallery Desktop View](assets/doc-images/cloud-runner-page-gallery-desktop.png)
  ![Gallery Mobile View](assets/doc-images/cloud-runner-page-gallery-mobile.png)

- **Get Updates (`updates.html`)**
  ![Get Updates Desktop View](assets/doc-images/cloud-runner-page-updates-desktop.png)
  ![Get Updates Mobile View](assets/doc-images/cloud-runner-page-updates-mobile.png)

- **Soundtrack (`music.html`)**
  ![Soundtrack Desktop View](assets/doc-images/cloud-runner-page-music-desktop.png)
  ![Soundtrack Mobile View](assets/doc-images/cloud-runner-page-music-mobile.png)

- **Thank You (`thank-you.html`)**
  ![Thank You Desktop View](assets/doc-images/cloud-runner-page-thank-you-desktop.png)
  ![Thank You Mobile View](assets/doc-images/cloud-runner-page-thank-you-mobile.png)

### W3C HTML & CSS Validation

Validated on `2026-11-22` via W3C Nu Html Checker and W3C CSS Checker—all five HTML pages and `assets/css/styles.css` passed with **0 errors and 0 warnings**.

- **Home (`index.html`)**
  ![W3C HTML Validation — Home](assets/doc-images/cloud-runner-index-page-W3C-HTML-CSS-validation-pass.png)
- **Gallery (`gallery.html`)**
  ![W3C HTML Validation — Gallery](assets/doc-images/cloud-runner-gallery-page-W3C-HTML-CSS-validation-pass.png)
- **Get Updates (`updates.html`)**
  ![W3C HTML Validation — Get Updates](assets/doc-images/cloud-runner-updates-page-W3C-HTML-CSS-validation-pass.png)
- **Soundtrack (`music.html`)**
  ![W3C HTML Validation — Soundtrack](assets/doc-images/cloud-runner-music-page-W3C-HTML-CSS-validation-pass.png)
- **Thank You (`thank-you.html`)**
  ![W3C HTML Validation — Thank You](assets/doc-images/cloud-runner-thank-you-page-W3C-HTML-CSS-validation-pass.png)
- **Stylesheet (`assets/css/styles.css`)**
  ![W3C CSS Validation — Stylesheet](assets/doc-images/cloud-runner-css-styles-W3C-HTML-CSS-validation-pass.png)

### Lighthouse Audits (Desktop & Mobile)

Audited in Chrome DevTools (Incognito) against the live GitHub Pages site, comparing the `2026-11-20` baseline against the `2026-11-22` pass after WebP optimization, preload/priority tuning, and viewport/background sizing updates (`100svh`, `min-height: 500px`, `background-size: cover`).

| Page | Viewport | First Test (`2026-11-20`)<br>Perf / Acc / BP / SEO | Latest Test (`2026-11-22`)<br>Perf / Acc / BP / SEO | Perf Delta |
| :--- | :--- | :---: | :---: | :---: |
| `index.html` | Desktop | 95 / 100 / — / 100 | **99 / 100 / 96 / 100** | +4 |
| `index.html` | Mobile | 94 / 100 / — / 100 | **96 / 100 / 96 / 100** | +2 |
| `gallery.html` | Desktop | 80 / 100 / — / 100 | **99 / 100 / 100 / 100** | +19 |
| `gallery.html` | Mobile | 73 / 100 / — / 100 | **89 / 100 / 100 / 100** | +16 |
| `updates.html` | Desktop | 61 / 100 / — / 100 | **100 / 100 / 100 / 100** | +39 |
| `updates.html` | Mobile | 98 / 100 / — / 100 | **97 / 100 / 100 / 100** | -1 |
| `music.html` | Desktop | *Not recorded in first set* | **100 / 100 / 100 / 100** | — |
| `music.html` | Mobile | *Not recorded in first set* | **97 / 100 / 100 / 100** | — |
| `thank-you.html` | Desktop | 85 / 98 / 100 / 100 | **100 / 98 / 100 / 100** | +15 |
| `thank-you.html` | Mobile | 97 / 98 / 100 / 100 | **97 / 98 / 100 / 100** | 0 |

*(Note: `game.html` was included in the `2026-11-20` baseline at 100 / 100 / 100 / 100 desktop and 97 / 100 / 100 / 100 mobile; `music.html` was audited in the `2026-11-22` pass.)*

- **Home (`index.html`)**
  
  ![Lighthouse Desktop — Home](assets/doc-images/cloud-runner-lighthouse-index-page-desktop-check.jpeg)

  ![Lighthouse Mobile — Home](assets/doc-images/cloud-runner-lighthouse-mobile-check.png)
  
- **Gallery (`gallery.html`)**
  
  ![Lighthouse Desktop — Gallery](assets/doc-images/cloud-runner-lighthouse-gallery-desktop-check.jpeg)

  ![Lighthouse Mobile — Gallery](assets/doc-images/cloud-runner-lighthouse-gallery-mobile-check.png)
  
- **Get Updates (`updates.html`)**
  
  ![Lighthouse Desktop — Get Updates](assets/doc-images/cloud-runner-lighthouse-updates-desktop-check.jpeg)
  
  ![Lighthouse Mobile — Get Updates](assets/doc-images/cloud-runner-lighthouse-updates-mobile-check.png)
  
- **Soundtrack (`music.html`)**
  
  ![Lighthouse Desktop — Soundtrack](assets/doc-images/cloud-runner-lighthouse-music-desktop-check.jpeg)
  
  ![Lighthouse Mobile — Soundtrack](assets/doc-images/cloud-runner-lighthouse-music-mobile-check.png)
  
- **Thank You (`thank-you.html`)**
  
  ![Lighthouse Desktop — Thank You](assets/doc-images/cloud-runner-lighthouse-thankyou-desktop-check.jpeg)
  
  ![Lighthouse Mobile — Thank You](assets/doc-images/cloud-runner-lighthouse-thankyou-mobile-check.png)

## Credits, Attribution & Ownership

- **Original Concept & IP:** *Cloud Runner*—including its premise, floating-island world-building, characters (including the five teenage scavengers led by **Rowan Cole**, **Toby Cole**, **Jules Mercer**, **Marek Hale**, and **Kieran Hale**, alongside **Silver Vane** and **Caspian Vane**), site copy, and web implementation—is an original concept by **Raf Joseph (`raf-src`)**.
- **Copyright Notice:** © 2026 Raf Joseph. All rights reserved. Original written narrative, character descriptions, site copy, and custom code in this repository may not be reproduced, redistributed, or adapted into derivative works without permission.
- **Visual & Audio Assets:** Teaser visuals, character portraits, and hero imagery and video were generated using **Google Flow** 
- **Libraries, Fonts & Mentorship:** Built with **Bootstrap 5**, **Google Fonts (`Inter`)**, and **Font Awesome** under their respective licenses, with guidance and feedback from bootcamp tutors and peers at WAES and Code Institute.

## Declaration of Use of AI

- **Media Generation:** **Google Flow** was used to generate promotional teaser visuals, character artwork, and video for *Cloud Runner*.
- **Development & Documentation Support:** **GitHub Copilot** (VS Code *Ask* mode) and **Google Gemini** were used for consultative troubleshooting, CSS/validation/Lighthouse checks, and README organization.
- **Author Responsibility:** All HTML, CSS, Bootstrap integration, testing, and final commits were reviewed and verified by the author.

## Future Features

Planned enhancements and future expansions for *Cloud Runner* beyond the initial promotional release:

- **Interactive Dropdown Button on Home (`index.html`):** Add a clean dropdown menu on the home page for quick jumping to sections or screening/release options without cluttering the top navigation bar.
- **Ticket Booking Form at Launch:** Introduce a dedicated ticket booking flow and screening finder once *Cloud Runner* approaches its theatrical release window.
- **Official Music Video Showcase:** Embed or feature the official *"Skybound"* music video alongside visual teasers and behind-the-scenes clips.
- **Full Soundtrack Tracklist (Song & Artist Credits):** Expand the soundtrack page with a realistic, structured tracklist listing each song title, featured artist/composer, and track details to build out the film's audio identity.
- **Spotify Soundtrack Playlist Link:** Add a direct link (and optional embedded player) to an official *Cloud Runner* soundtrack playlist on Spotify so visitors can stream the score and related tracks.
