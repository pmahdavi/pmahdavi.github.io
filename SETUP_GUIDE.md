# Quick Setup Guide for GitHub Pages

## Step 1: Customize Your Content

Before publishing, replace all placeholder text with your actual information:

### In all HTML files:
- Replace `Your Name` with your actual name
- Replace `[Your Location]` with your location
- Replace `[Your Institution/Company]` with your affiliation
- Replace `your.email@example.com` with your email
- Update social media URLs with your profiles

### Specific pages to update:

#### `index.html` (Homepage)
- Update bio paragraphs
- Update news items with your actual achievements
- Add/remove news items as needed

#### `research.html`
- Add your actual publications
- Update research interests
- Add links to papers, code repositories, etc.

#### `blog.html`
- Add your actual blog posts
- Update dates and descriptions

#### `cv.html`
- Add your education history
- Add your work experience
- Add awards and honors
- Add service activities

## Step 2: Add Your Profile Picture

Replace `profile.jpg` with your own photo:
- Recommended size: 400x400 pixels or larger
- Should be square (1:1 aspect ratio)
- Good quality, professional photo
- Save as `profile.jpg` in the root directory

**Quick tip**: If you don't have a profile picture yet, you can temporarily remove the `<img>` tag from `index.html` or use a placeholder from a service like [UI Avatars](https://ui-avatars.com/).

## Step 3: Create GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click "New repository" (or go to https://github.com/new)
3. Name it: `yourusername.github.io` (replace `yourusername` with your actual GitHub username)
4. Make it **Public**
5. Click "Create repository"

## Step 4: Upload Your Files

### Option A: Using GitHub Web Interface (Easier)
1. In your new repository, click "uploading an existing file"
2. Drag and drop all files:
   - `index.html`
   - `research.html`
   - `blog.html`
   - `cv.html`
   - `styles.css`
   - `profile.jpg` (your photo)
   - `README.md`
   - `.gitignore`
3. Commit the changes

### Option B: Using Git Command Line
```bash
cd /Users/pxm5426/research/pouria
git init
git add .
git commit -m "Initial commit: Research portfolio website"
git branch -M main
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

## Step 5: Enable GitHub Pages

1. Go to your repository settings
2. Click "Pages" in the left sidebar
3. Under "Source", select "main" branch
4. Click "Save"
5. Wait 1-2 minutes for deployment

## Step 6: Visit Your Site!

Your site will be live at: `https://yourusername.github.io`

## Customization Tips

### Change Colors
Edit the CSS variables in `styles.css`:
```css
:root {
    --primary-color: #2c3e50;      /* Main headings */
    --secondary-color: #3498db;    /* Accent color */
    --link-color: #3498db;         /* Link color */
    /* ... more variables */
}
```

### Add Google Analytics
Add this code before `</head>` in all HTML files:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR-GA-ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR-GA-ID');
</script>
```

### Add MathJax for Equations
Add this before `</head>` in pages where you need math:
```html
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
```

## Need Help?

- **GitHub Pages Documentation**: https://docs.github.com/en/pages
- **Markdown Guide**: https://www.markdownguide.org/ (for README)
- **CSS Reference**: https://developer.mozilla.org/en-US/docs/Web/CSS

## Future Enhancements

Consider adding:
- Individual blog post pages
- A projects showcase page
- Dark mode toggle
- Search functionality
- RSS feed for blog
- Integration with Jekyll for easier blog management

Good luck with your research portfolio! 🚀

---

**Built with modern web technologies**: HTML5, CSS3, Glassmorphism design, smooth animations, and responsive layout.
