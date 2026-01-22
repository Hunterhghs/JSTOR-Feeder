# H Heuristics Research Initiative - JSTOR Feeder

A scholarly website for showcasing academic research publications intended for JSTOR distribution.

## 🚀 Quick Start

### Deploying to Cloudflare Pages

1. Push this repository to GitHub: `https://github.com/Hunterhghs/JSTOR-Feeder.git`
2. Go to [Cloudflare Pages](https://pages.cloudflare.com/)
3. Connect your GitHub account and select the `JSTOR-Feeder` repository
4. Configure build settings:
   - **Build command:** (leave empty - static site)
   - **Build output directory:** `/` (root)
5. Deploy!

---

## 📁 Project Structure

```
JSTOR-Feeder/
├── index.html          # Main website page
├── styles.css          # All styling
├── script.js           # Interactive features
├── content/
│   ├── pdfs/          # PDF research publications
│   └── images/        # Images for the website
├── assets/            # Additional assets (logos, icons)
└── README.md          # This file
```

---

## ➕ Adding New Content

### Adding a New PDF Publication

1. **Add the PDF file** to the `content/pdfs/` folder

2. **Add a new publication card** to `index.html`. Find the `<div class="publications-grid">` section and add:

```html
<!-- New Publication Card -->
<article class="publication-card">
    <div class="card-accent"></div>
    <div class="card-content">
        <span class="publication-type">Research Report</span>
        <h3 class="publication-title">Your Publication Title</h3>
        <p class="publication-excerpt">
            A brief description of the publication content (2-3 sentences).
        </p>
        <div class="publication-meta">
            <span class="meta-item">
                <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                    <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path>
                    <polyline points="14 2 14 8 20 8"></polyline>
                </svg>
                PDF
            </span>
        </div>
        <div class="publication-actions">
            <a href="content/pdfs/Your-File-Name.pdf" target="_blank" class="btn btn-primary">
                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                    <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"></path>
                    <polyline points="15 3 21 3 21 9"></polyline>
                    <line x1="10" y1="14" x2="21" y2="3"></line>
                </svg>
                Open in Browser
            </a>
            <a href="content/pdfs/Your-File-Name.pdf" download class="btn btn-secondary">
                <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                    <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"></path>
                    <polyline points="7 10 12 15 17 10"></polyline>
                    <line x1="12" y1="15" x2="12" y2="3"></line>
                </svg>
                Download
            </a>
        </div>
    </div>
</article>
```

3. **Update the file path** in both `href` attributes to match your PDF filename

4. **Commit and push** to GitHub - Cloudflare will auto-deploy

### Adding Images

1. Place images in the `content/images/` folder
2. Reference them in HTML: `<img src="content/images/your-image.jpg" alt="Description">`

### Changing Publication Types

You can customize the publication type badge. Common options:
- `Research Report`
- `Working Paper`
- `Policy Brief`
- `Technical Report`
- `White Paper`
- `Journal Article`

---

## 🎨 Customization

### Updating Colors

Edit the CSS variables in `styles.css` at the top of the file:

```css
:root {
    --color-forest: #1e3a2f;      /* Primary dark green */
    --color-gold: #b8860b;         /* Accent gold */
    --color-parchment: #f7f4ed;    /* Background cream */
    /* ... more colors */
}
```

### Updating Contact Email

Find this line in `index.html` and change the email:

```html
<a href="mailto:research@hheuristics.org" class="btn btn-accent">
```

### Adding New Sections

Copy the section structure pattern used in the existing sections.

---

## 📄 File Naming Conventions

- **PDFs:** Use descriptive names with spaces or hyphens
  - ✅ `The Great Convergence.pdf`
  - ✅ `technological-diffusion-2026.pdf`
  
- **Images:** Use lowercase with hyphens
  - ✅ `research-team-photo.jpg`
  - ✅ `chart-convergence-data.png`

---

## 🔄 Updating the Website

1. Make your changes locally
2. Commit: `git add . && git commit -m "Added new publication"`
3. Push: `git push origin main`
4. Cloudflare Pages will automatically rebuild and deploy (usually within 1-2 minutes)

---

## 📞 Support

For technical issues with the website, check the [Cloudflare Pages documentation](https://developers.cloudflare.com/pages/).

---

*H Heuristics Research Initiative - Advancing Knowledge Through Open Research*
