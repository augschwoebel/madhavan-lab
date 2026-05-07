# Madhavan Lab Website

Static website for the Madhavan Lab, Department of Physics, University of Illinois Urbana-Champaign.

## Structure

```
madhavan-lab/
├── index.html              ← Home page
├── css/
│   └── style.css           ← All styles
├── js/
│   └── main.js             ← Navigation & shared JS
├── images/                 ← Put all your images here
│   └── (favicon.png, photos, STM images, etc.)
└── pages/
    ├── about.html          ← About / PI page
    ├── research.html       ← Research topics
    ├── people.html         ← Lab members + alumni
    ├── lab.html            ← Instruments
    ├── publications.html   ← Publications by year
    └── blog.html           ← Blog / news
```

## Hosting on GitHub Pages

1. Create a new GitHub repository named `madhavan-lab` (or your preferred name).
2. Upload all files in this folder to the repository (maintain the folder structure).
3. Go to **Settings → Pages** in your repository.
4. Under "Source", select **Deploy from a branch** → `main` → `/ (root)`.
5. Click Save. Your site will be live at `https://<your-username>.github.io/madhavan-lab/`.

**Custom domain**: If you have `madhavan.physics.illinois.edu` or similar, add a `CNAME` file at the root containing just your domain name.

## How to Edit

### Adding a person (People page)
Copy a `person-card` div block and update:
- Replace the `img-placeholder` with `<img src="../images/your-photo.jpg" class="person-card__photo" alt="Name">`
- Update name, role, and email

### Adding a publication (Publications page)
Copy a `pub-entry` div block under the correct year group. Increment the number.
Add new `pub-year-group` blocks for new years at the top.

### Adding a blog post (Blog page)
Copy a `blog-card` div block and update the date, category, title, excerpt, and link.

### Adding an instrument (The Lab page)
Copy an `instrument-card` div block and update images, specs, and description.

### Adding a research topic (Research page)
Copy a `research-topic` div block. Alternating topics automatically reverse layout (image left/right).

### Replacing placeholder images
All `img-placeholder` divs are stand-ins. Replace them with:
```html
<img src="../images/your-image.jpg" alt="Description" class="[matching class]">
```
Place all images in the `/images/` folder.

## Colors (UIUC Branded)
- Illini Blue: `#13294b`
- Illini Orange: `#e84a27`

## Fonts
- Headings: EB Garamond (Google Fonts)
- Body: DM Sans (Google Fonts)
- Monospace accents: DM Mono (Google Fonts)
