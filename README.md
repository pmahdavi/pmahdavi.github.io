# Pouria Mahdavinia - Research Portfolio

A clean, modern personal website showcasing research in optimization theory, efficient AI systems, and LLM training methods with a sophisticated glassmorphic design.

## Features

- **Clean, professional design** with responsive layout
- **Multiple pages**: About, Research, and Blog
- **Social media integration** (Twitter/X, GitHub, Google Scholar, LinkedIn)
- **Fully customizable** with CSS variables for easy theming
- **Mobile-friendly** design that works on all devices

## Setup Instructions

### Deploying to GitHub Pages

1. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "Personalize website with research info"
   git push origin main
   ```

2. **Enable GitHub Pages** (if not already enabled):
   - Go to repository settings
   - Navigate to "Pages" in the left sidebar
   - Select "main" branch as the source
   - Save and wait a few minutes for deployment

3. **Visit your site** at `https://pmahdavi.github.io`

## Updating Content

### Adding Publications
Edit `research.html` to add new publications in the Publications or Preprints section. Each paper follows this structure:
```html
<article class="paper">
    <h3><a href="#">Paper Title</a></h3>
    <p class="authors"><strong>Pouria Mahdavinia</strong>, Coauthors</p>
    <p class="venue">Conference/Journal Year</p>
    <p class="description">Description of contributions</p>
    <div class="paper-links">
        <a href="https://github.com/..." class="paper-link">Code</a>
    </div>
</article>
```

### Adding Blog Posts
When ready to add blog content:
1. Create individual blog post HTML files
2. Update `blog.html` to replace the "Coming soon" message with post previews
3. Link each preview to its full post page

### Updating CV
Edit `cv.html` to add new experiences, awards, or skills.

## Optional Enhancements

- Add **Google Analytics** for visitor tracking
- Integrate with **Jekyll** for easier blog management
- Add a **dark mode** toggle
- Include **MathJax** or **KaTeX** for mathematical equations
- Add **syntax highlighting** for code snippets

## License

Feel free to use this template for your own website.
