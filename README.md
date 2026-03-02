# AligsCare Website

Static, single-page website for AligsCare, a Houston-based 501(c)(3) providing cancer care support through Jawaharlal Nehru Medical College (JNMC), Aligarh Muslim University, India.

## Stack
- Pure static site (`index.html` + image assets)
- No build step
- No framework dependencies

## Project Structure
- `index.html`: all markup, CSS, and JavaScript
- `assets/images/`: section images, team/founder images, and gallery photos
- `assets/images/galleries/<program>/`: modal gallery images for each impact card

## Local Preview
Open `index.html` directly in a browser, or run a local static server:

```powershell
python -m http.server 5173
```

Then visit `http://localhost:5173`.

## Current Site Features
- Story-driven landing page sections (hero, story, programs, impact, team, donate, footer)
- Impact cards with clickable photo galleries (keyboard accessible)
- Expanded "What This Looks Like in Practice" program cards with per-program image sets
- Founder spotlight and centered team/advisor layout
- Donation methods (PayPal, Zelle, Check)

## Editing Guide
Most edits happen in `index.html`.

### Update copy or layout
- Edit section HTML directly
- Adjust styling in embedded CSS blocks

### Update images
- Card cover images are controlled by `.story-card-visual.<key>` CSS rules
- Gallery photos are defined in the `impactGalleries` JavaScript object

### Add a new impact program card with gallery
1. Add a new card in the "What This Looks Like in Practice" grid with `data-gallery="<key>"`.
2. Add or update the corresponding `.story-card-visual.<key>` CSS class for the cover image.
3. Add a matching `<key>` entry in `impactGalleries` with `title` and `images`.
4. Place image files under `assets/images/galleries/<folder>/` and reference them in `impactGalleries`.
5. Verify keyboard and click behavior still works in the modal.

Note: `data-gallery` keys in card markup must exactly match keys in `impactGalleries`.

## Deployment
This is a static site. Push to `main` and Vercel auto-deploys.

## License
All rights reserved by AligsCare unless stated otherwise.
