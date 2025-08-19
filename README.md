# Victor Nyabuti Ong'era - Academic Website

This is the personal academic website for Victor Nyabuti Ong'era, a PhD Candidate in Linguistics specializing in theoretical syntax, language acquisition, and experimental linguistics.

## Website Features

- **Professional Design**: Clean, modern academic website design
- **Responsive Layout**: Works perfectly on desktop, tablet, and mobile devices
- **Research Showcase**: Dedicated sections for research projects and publications
- **Contact Information**: Easy access to professional contact details
- **News Section**: Updates on recent activities and achievements

## Quick Start

### Option 1: Simple HTML Version (Recommended)

The website includes a complete HTML version (`index.html`) that works immediately with GitHub Pages without any build process.

1. **Push to GitHub**: Upload all files to your GitHub repository
2. **Enable GitHub Pages**: 
   - Go to your repository settings
   - Scroll down to "GitHub Pages" section
   - Select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Click "Save"

3. **Your website will be live** at `https://ongevic.github.io`

### Option 2: Jekyll Version (Advanced)

If you prefer to use the Jekyll version for more dynamic features:

1. **Install Ruby and Jekyll** (if not already installed)
2. **Install dependencies**: `bundle install`
3. **Run locally**: `bundle exec jekyll serve`
4. **Deploy**: Push to GitHub and enable GitHub Pages with Jekyll source

## File Structure

```
website/
├── index.html              # Main HTML version (ready to deploy)
├── _config.yml             # Jekyll configuration
├── Gemfile                 # Ruby dependencies
├── index.md                # Jekyll homepage
├── _layouts/               # Jekyll layout templates
├── _projects/              # Research project pages
├── _publications/          # Publication pages
├── assets/                 # CSS and other assets
└── README.md               # This file
```

## Customization

### Update Personal Information

1. **Name and Title**: Update in `index.html` (lines 4, 5, 89, 90)
2. **Contact Information**: Update email and social links in the contact section
3. **Research Areas**: Modify the research interests in the About section
4. **Publications**: Add your actual publications to the publications section
5. **Profile Image**: Replace the placeholder "VO" with your actual photo

### Styling

The website uses CSS custom properties for easy theming:

```css
:root {
    --primary-color: #2563eb;      /* Main brand color */
    --secondary-color: #7c3aed;    /* Secondary brand color */
    --text-color: #1f2937;         /* Main text color */
    --text-secondary: #6b7280;     /* Secondary text color */
    --bg-color: #ffffff;           /* Background color */
    --card-bg: #f9fafb;            /* Card background color */
    --border-color: #e5e7eb;       /* Border color */
}
```

## Content Sections

### About Section
- Personal introduction
- Research interests
- Academic background

### Research Section
- Current research projects
- Methodology descriptions
- Key findings

### Publications Section
- Academic publications
- Journal articles
- Conference papers
- DOI links

### News Section
- Recent achievements
- Conference presentations
- Awards and recognition

### Contact Section
- Email address
- Social media links
- Professional profiles

## Browser Support

The website is compatible with:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Performance

- Optimized CSS and JavaScript
- Fast loading times
- Mobile-responsive design
- SEO-friendly structure

## Deployment Status

✅ **Ready for GitHub Pages deployment**
✅ **No build process required**
✅ **Mobile responsive**
✅ **Professional design**

## Support

If you encounter any issues:

1. Check that all files are uploaded to your GitHub repository
2. Ensure GitHub Pages is enabled in repository settings
3. Wait a few minutes for changes to propagate
4. Clear your browser cache if needed

## License

This website template is provided for academic use. Feel free to modify and adapt for your own academic website.

---

**Victor Nyabuti Ong'era**  
PhD Candidate in Linguistics  
Email: victor.ongera@example.com  
GitHub: [ongevic](https://github.com/ongevic)
