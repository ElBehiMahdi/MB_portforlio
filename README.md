# MB Portfolio

A blazing-fast, lightweight portfolio website built with pure HTML, CSS, and JavaScript. Zero dependencies, zero build step, instant deployment.

## Live Demo

[https://elbehimahdi.github.io/MB_portforlio/](https://elbehimahdi.github.io/MB_portforlio/)

## Tech Stack

- **HTML5** - Semantic structure
- **CSS3** - Modern styling with CSS variables, flexbox, grid
- **Vanilla JavaScript** - Theme toggle, mobile menu, scroll animations

## Features

- Dark/Light theme toggle (persists via localStorage)
- Responsive mobile-first design
- Smooth scroll navigation
- Auto-hiding navbar on scroll
- Scroll-triggered fade-in animations
- SEO-friendly semantic markup

## Sections

| Section | Description |
|---------|-------------|
| **Hero** | Introduction with name, title, and CTA buttons |
| **Skills** | Categorized skill tags (Languages, Frontend, Backend, Tools) |
| **Experience** | Timeline-style work history |
| **Blog** | Static blog post cards linking to full articles |
| **Contact** | Call-to-action with social links |

## Project Structure

```
portfolio_mb/
├── index.html              # Main page (all sections)
├── css/
│   └── style.css           # All styles with dark/light themes
├── js/
│   └── main.js             # Theme toggle, mobile menu, scroll animations
├── blog/
│   ├── getting-started-with-astro.html
│   ├── performance-tips.html
│   └── career-advice.html  # Sample blog posts
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Pages auto-deployment
├── vercel.json             # Vercel deployment config
├── netlify.toml            # Netlify deployment config
└── README.md               # This file
```

## Getting Started

### Prerequisites

None. This is a static site with no dependencies.

### Local Development

Serve the files locally with any HTTP server:

```bash
# Using Python (pre-installed on most systems)
python3 -m http.server 8080

# Using PHP
php -S localhost:8080

# Using Node.js
npx serve .
```

Open `http://localhost:8080` in your browser.

### Customizing Content

Search for these placeholders in `index.html` and replace them:

| Placeholder | Replace With |
|-------------|--------------|
| `[Your Name]` | Your actual name |
| `[Your Name]` in `<title>` | Your name |
| `your.email@example.com` | Your email |
| `https://github.com/yourusername` | Your GitHub profile URL |
| `https://linkedin.com/in/yourusername` | Your LinkedIn URL |
| `https://twitter.com/yourusername` | Your X/Twitter URL |
| `placeholder-avatar` div | Replace with `<img src="your-photo.jpg" alt="Your Name">` |

Update the skills, experience entries, and blog posts with your own content.

### Adding Blog Posts

1. Create a new `.html` file in the `blog/` directory
2. Copy an existing post as a template
3. Update the title, date, content, and meta tags
4. Add a card in the blog section of `index.html` linking to your new post

### Changing Colors

CSS variables are defined at the top of `css/style.css`. Modify these to change the theme:

```css
:root {
    --bg-primary: #0a192f;      /* Main background */
    --accent: #64ffda;           /* Accent color */
    --text-heading: #ffffff;     /* Heading text */
    /* ... more variables */
}
```

## Deployment

### GitHub Pages (Current)

1. Push to `main` branch
2. Go to **Settings > Pages** in your repo
3. Select **Source: Deploy from a branch** → `main` → `/ (root)`
4. Your site is live at `https://<username>.github.io/<repo>/`

Deployment is automated via `.github/workflows/deploy.yml` but requires enabling Pages in settings as described above.

### Vercel

1. Go to [vercel.com](https://vercel.com)
2. Import your GitHub repo
3. Click Deploy

Config: `vercel.json`

### Netlify

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag the entire project folder onto the page

Config: `netlify.toml`

### Cloudflare Pages

1. Go to [dash.cloudflare.com/pages](https://dash.cloudflare.com/pages)
2. Connect your GitHub repo
3. Build settings: leave empty (static site)

## GitHub Pages Limitations

| Limitation | Impact on Portfolio |
|-----------|---------------------|
| No server-side code | Not applicable (static site) |
| 1GB repo size limit | Fine for portfolios |
| 100GB bandwidth/month | Supports millions of visits |
| Public repo required | Code is visible to everyone |
| No environment variables | Not needed for static sites |
| No form handling backend | Use third-party services (Formspree, Netlify Forms) |

## Workflow

```
main (production, auto-deployed)
  ↑
dev (development branch)
```

1. Make changes on `dev`
2. Test locally
3. Push `dev` and open a Merge Request/PR to `main`
4. Merge to deploy

## License

MIT
