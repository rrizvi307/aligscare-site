# AligsCare Website

Static, single-page website for AligsCare, a Houston-based 501(c)(3) providing cancer care support through Jawaharlal Nehru Medical College (JNMC), Aligarh Muslim University, India.

## What’s Included
- `index.html` with all content, styles, and scripts in one file
- No build step or dependencies

## Local Preview
Open `index.html` in a browser.

Optional: serve locally to avoid file URL restrictions.
```powershell
python -m http.server 5173
```
Then visit `http://localhost:5173`.

## Content Highlights
- Hero, story, programs, impact, team, and donate sections
- Impact counters and scroll-triggered animations
- Donation methods (PayPal, Zelle, Check)
- Contact and footer details

## Editing
All copy, styles, and scripts live in `index.html`.

Common updates:
- Text and section content: edit HTML directly
- Colors and typography: update CSS variables under `:root`
- Impact numbers: update `data-target` attributes in the impact strip
- Donation links or addresses: update the donate section

## Deployment
This is a static site. Deploy by serving `index.html` from any static host (GitHub Pages, Netlify, Vercel, S3, etc.).

## License
All rights reserved by AligsCare unless stated otherwise.
