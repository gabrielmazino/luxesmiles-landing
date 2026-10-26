# Luxe Smiles Landing Page

The public website for **Luxe Smiles Dental Center**, a patient-centered, multi-specialty dental clinic with branches in Southwoods City, Biñan, and Sta. Rosa, Laguna, Philippines.

🔗 **Live site:** https://luxesmilesdentalcenter.netlify.app/

This is a single-page static site (plain HTML, CSS and a little vanilla JavaScript). It has no build step, framework or backend.

> The clinic's management system (with the database and backend) is a separate project: [luxesmilesdental](https://github.com/gabrielmazino/luxesmilesdental).

## Features

- **Hero section**: headline, booking and call buttons, and a photo collage of the clinic
- **Sliding highlights (marquee)**: the clinic's social posts scroll in a seamless loop and pause on hover
- **About**: the team and the clinic's approach to care
- **Services**: three featured treatments plus a grid of other treatments offered
- **Facilities**: photos of the treatment rooms and equipment
- **Locations**: both branches with tap-to-call numbers, an embedded Google Map and a directions link
- **Booking call-to-action**: call either branch, message on Facebook, or email
- **Responsive**: floating rounded header, mobile hamburger menu and a fixed "Call now / Directions" bar on phones
- **Accessible**: skip link, alt text, keyboard focus styles, and `prefers-reduced-motion` support (animations turn off)
- **Fast**: images are compressed WebP (~700 KB for the whole site)

## Tech stack

| Part | Used |
| --- | --- |
| Markup | HTML5 |
| Styling | CSS (custom properties, Grid, Flexbox, keyframe animations) |
| Scripts | Vanilla JavaScript (mobile menu, header shadow, scroll reveal) |
| Fonts | [Fraunces](https://fonts.google.com/specimen/Fraunces) (headings) and [Inter](https://fonts.google.com/specimen/Inter) (body), from Google Fonts |
| Hosting | [Netlify](https://www.netlify.com/) |

## Project structure

```
luxesmiles-landing/
├── public/              # Everything that gets deployed
│   ├── index.html       # The whole page
│   ├── styles.css       # All styles
│   └── images/          # Optimized WebP photos, logo and favicons
└── README.md
```

## Running locally

No install needed. Either:

- Open `public/index.html` in your browser, **or**
- Serve the folder (recommended, so the embedded map loads correctly):

  ```bash
  npx serve public
  # or
  python -m http.server 8000 --directory public
  ```

  Then visit http://localhost:3000 (serve) or http://localhost:8000 (Python).

## Deployment

The site is hosted on Netlify with **`public`** as the publish directory.

**Option A: Drag and drop**
1. Open the site in the [Netlify dashboard](https://app.netlify.com/) → **Deploys**.
2. Drag the `public` folder into the upload box.

**Option B: Auto-deploy from GitHub**
1. In Netlify: **Site configuration → Build & deploy → Link repository** and pick this repo.
2. Leave **Build command** empty and set **Publish directory** to `public`.
3. Every push to `main` then updates the live site automatically.

## Editing content

- **Text, phone numbers and links** are all in `public/index.html`.
- **Colors and fonts** are CSS variables at the top of `public/styles.css` (`--green`, `--green-deep`, `--serif`, `--sans`, …).
- **Images:** add new photos to `public/images/` as `.webp` (about 900px wide is plenty), then update the matching `<img src="...">` in `index.html`. The marquee images appear in **both** marquee groups, so update both when you change them.

## Contact (clinic)

- **Southwoods Branch:** B303 Enterprise Ave, Coral Center Building, Southwoods City, Biñan, Laguna · 0917 329 3588 / 0994 616 0475
- **Sta. Rosa Branch:** 0966 845 2952
- **Email:** luxesmilesdc@gmail.com
- **Facebook:** [facebook.com/luxesmilesdc](https://www.facebook.com/luxesmilesdc)

## Credits

Designed and built by [@gabrielmazino](https://github.com/gabrielmazino) as a personal project.

Photos, logo and branding belong to Luxe Smiles Dental Center. All rights reserved. They are **not** covered by any open-source license and may not be reused.
