# Personal Research Website

A modern, easy-to-edit personal research website built with Jekyll. Perfect for academics, researchers, and professionals who want to showcase their work online.

## Features

- 🎨 **Modern Design**: Clean, professional design with responsive layout
- 📝 **Easy Content Management**: Simple markdown files for adding new content
- 📚 **Publications Section**: Organized display of research papers and publications
- 🔬 **Projects Section**: Showcase current and past research projects
- 📱 **Mobile Responsive**: Looks great on all devices
- 🚀 **GitHub Pages Ready**: Easy deployment to GitHub Pages
- 🔍 **SEO Optimized**: Built-in SEO features for better visibility
- ⚡ **Fast Loading**: Optimized for performance

## Quick Start

### 1. Prerequisites

- Ruby (version 2.6 or higher)
- RubyGems
- Git

### 2. Installation

```bash
# Clone this repository
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name

# Install dependencies
bundle install

# Start the development server
bundle exec jekyll serve
```

Visit `http://localhost:4000` to see your website!

## Content Management

### Adding Publications

1. Create a new file in the `_publications` folder
2. Use the following format:

```markdown
---
layout: publication
title: "Your Paper Title"
authors: "Your Name, Co-author Name"
venue: "Conference/Journal Name"
year: 2024
doi: "10.1000/example.doi"
excerpt: "Brief description of the paper"
---

Your paper content goes here...
```

### Adding Projects

1. Create a new file in the `_projects` folder
2. Use the following format:

```markdown
---
layout: project
title: "Project Title"
excerpt: "Brief project description"
status: "Active" # Active, Completed, or Planned
start_date: 2023-01
end_date: 2024-12
funding: "Funding Agency"
team: "Your Name (PI), Collaborator Name"
---

Your project content goes here...
```

### Customizing Your Profile

Edit the following files to personalize your website:

- `_config.yml`: Update your name, email, and basic information
- `index.md`: Modify the homepage content
- `assets/images/profile.jpg`: Replace with your profile photo

## File Structure

```
├── _config.yml          # Site configuration
├── _layouts/            # HTML templates
│   ├── default.html     # Main layout
│   ├── publication.html # Publication page layout
│   └── project.html     # Project page layout
├── _publications/       # Publication markdown files
├── _projects/          # Project markdown files
├── assets/             # Static assets
│   ├── css/            # Stylesheets
│   └── images/         # Images
├── index.md            # Homepage
└── README.md           # This file
```

## Deployment to GitHub Pages

### Option 1: Automatic Deployment

1. Push your code to GitHub
2. Go to your repository settings
3. Navigate to "Pages" section
4. Select "GitHub Actions" as the source
5. Create a new workflow file in `.github/workflows/jekyll.yml`:

```yaml
name: Deploy Jekyll site to Pages

on:
  push:
    branches: ["main"]
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: "pages"
  cancel-in-progress: false

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Setup Ruby
        uses: ruby/setup-ruby@v1
        with:
          ruby-version: '3.1'
          bundler-cache: true
      - name: Setup Pages
        uses: actions/configure-pages@v4
      - name: Build with Jekyll
        run: bundle exec jekyll build --baseurl "${{ steps.dependency-review-action.outputs.base-url }}"
        env:
          JEKYLL_ENV: production
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: ./_site

  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

### Option 2: Manual Deployment

```bash
# Build the site
bundle exec jekyll build

# The built site will be in the _site folder
# Upload the contents of _site to your web server
```

## Customization

### Colors and Styling

Edit `assets/css/main.css` to customize colors and styling. The main color variables are:

```css
:root {
  --primary-color: #2c3e50;    /* Main brand color */
  --secondary-color: #3498db;  /* Accent color */
  --accent-color: #e74c3c;     /* Call-to-action color */
  --text-color: #333;          /* Text color */
  --light-gray: #f8f9fa;       /* Background color */
}
```

### Adding New Sections

1. Create a new layout in `_layouts/` if needed
2. Add the page content in markdown format
3. Update navigation in `_layouts/default.html`

## Tips for Easy Editing

1. **Use Markdown**: All content is written in simple markdown format
2. **Front Matter**: Use YAML front matter for metadata (title, date, etc.)
3. **Images**: Place images in `assets/images/` and reference them with relative paths
4. **Links**: Use relative links for internal pages (e.g., `/publications/`)
5. **Preview**: Always preview changes locally before deploying

## Common Tasks

### Adding a New Publication

```bash
# Create a new file
touch _publications/your-paper-title.md

# Edit the file with your content
# The file will automatically appear on your website
```

### Updating Your Profile

```bash
# Edit the main page
nano index.md

# Update configuration
nano _config.yml
```

### Adding a Profile Photo

```bash
# Replace the profile image
cp your-photo.jpg assets/images/profile.jpg
```

## Support

If you encounter any issues:

1. Check that all dependencies are installed: `bundle install`
2. Ensure you're using a compatible Ruby version
3. Check the Jekyll documentation: https://jekyllrb.com/docs/
4. Create an issue in this repository

## License

This project is open source and available under the [MIT License](LICENSE).

## Contributing

Feel free to submit issues and enhancement requests!

---

**Happy Researching! 🚀**
