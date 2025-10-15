# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static research portfolio website built with pure HTML and CSS, designed for deployment on GitHub Pages. The site features a modern glassmorphic design with animations and responsive layouts, showcasing research publications, blog posts, and professional information.

## Architecture

### Multi-Page Structure
- **index.html**: Homepage with bio, profile picture, news updates, and social links
- **research.html**: Publications, preprints, and research interests
- **blog.html**: Blog post previews and links
- **cv.html**: Education, experience, awards, and service
- **styles.css**: Single unified stylesheet for all pages

### Design System
All styling is controlled through CSS variables defined in `:root` in styles.css:
- Color scheme uses gradients (`--gradient-1`, `--gradient-2`, `--gradient-3`)
- Primary colors: `--primary-color`, `--secondary-color`, `--accent-color`
- Spacing and layout: `--max-width: 900px`, `--spacing: 2rem`
- Typography uses system fonts with Georgia for headings

### Key CSS Features
- **Glassmorphism**: `backdrop-filter: blur()` with semi-transparent backgrounds
- **Animations**: Defined animations include `float`, `fadeInDown`, `slideInLeft`, `fadeInUp`, `shimmer`, `pulse`, `bounce`
- **Staggered animations**: `.news-list li:nth-child(n)` and `.paper:nth-child(n)` for entrance effects
- **Responsive breakpoints**: 768px and 480px

### Navigation Structure
- Sticky navbar with glassmorphic effect
- Active state indicated by `.nav-link.active`
- Underline animation on hover using `::after` pseudo-element

## Content Customization

### Placeholders to Replace
When customizing content, search for and replace:
- `Your Name` - appears in all HTML files
- `[Your Location]` - in bio section
- `[Your Institution/Company]` - in bio section
- `your.email@example.com` - contact email
- Social media URLs in `index.html` (Twitter, GitHub, Google Scholar, LinkedIn)
- Google Doc CV link: `YOUR_GOOGLE_DOC_ID`

### Adding Publications (research.html)
Publications use the `.paper` class structure:
```html
<article class="paper">
    <h3><a href="#">Title</a></h3>
    <p class="authors"><strong>Your Name</strong>, Coauthors</p>
    <p class="venue">Conference/Journal Year</p>
    <p class="description">Brief description</p>
    <div class="paper-links">
        <a href="#" class="paper-link">Paper</a>
        <a href="#" class="paper-link">Code</a>
    </div>
</article>
```

### Adding Blog Posts (blog.html)
Blog post previews use the `.blog-post-preview` class:
```html
<article class="blog-post-preview">
    <h2><a href="#">Title</a></h2>
    <p class="date">Date</p>
    <p class="excerpt">Preview text</p>
    <a href="#" class="read-more">Read more →</a>
</article>
```

### Adding News Items (index.html)
News items in `.news-list` support emoji icons:
```html
<li>
    <span class="emoji">📝</span>
    <span>News content with <a href="#">links</a>.</span>
</li>
```

## Deployment

### GitHub Pages Setup
1. Repository must be named `username.github.io`
2. Push all files to the `main` branch
3. Enable GitHub Pages in repository settings → Pages → Source: main branch
4. Site will be live at `https://username.github.io`

### Required Files
- index.html (required - entry point)
- research.html, blog.html, cv.html (navigation targets)
- styles.css (required - all styling)
- profile.jpg (recommended 400x400px or larger, 1:1 aspect ratio)

### Git Workflow
```bash
git add .
git commit -m "Description of changes"
git push origin main
```
Changes typically deploy within 1-2 minutes.

## Styling Modifications

### Changing Color Scheme
Edit CSS variables in styles.css:1-19. Gradients are used extensively for headings, buttons, and accents.

### Modifying Animations
- Disable animations: Set `animation: none` in respective classes
- Adjust timing: Modify animation duration in class definitions
- Stagger delays: Edit `animation-delay` in nth-child selectors

### Layout Adjustments
- Content width: Modify `--max-width` (default: 900px)
- Profile image size: `.profile-image` width/height (default: 240px)
- Responsive breakpoints: Adjust @media queries at 768px and 480px

## Optional Enhancements

The README suggests these additions:
- Google Analytics (add before `</head>`)
- MathJax for equations (add script tags for academic blog posts)
- Jekyll integration for blog management
- Dark mode toggle
- Individual blog post pages (copy structure from existing pages)

## Browser Compatibility

The site uses modern CSS features:
- `backdrop-filter` for glassmorphism (not supported in older browsers)
- CSS custom properties (variables)
- CSS Grid and Flexbox
- `prefers-reduced-motion` media query for accessibility
