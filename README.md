# Developer Portfolio Site

A Jekyll-based developer portfolio with an IDE-inspired design and syntax highlighting throughout. Built on the `jekyll-theme-console` base theme with extensive customizations.

## Features

- **IDE-Style Syntax Highlighting**: Custom SCSS with VS Code Dark+ color scheme
- **Responsive Design**: Mobile-first approach with flexible layouts
- **Portfolio Sections**: Projects, blog, resume, timeline, and contact
- **Collection-Based Content**: Easy management of projects and timeline entries
- **GitHub Pages Ready**: Configured for automatic deployment
- **SEO Optimized**: Built-in meta tags and sitemap generation

## Project Structure

```
portfolio-site/
├── _config.yml              # Jekyll configuration
├── Gemfile                  # Ruby dependencies
├── assets/
│   └── main-dark.scss       # Main stylesheet with imports
├── _sass/
│   ├── _ide-syntax.scss     # IDE-style syntax highlighting
│   └── _portfolio-custom.scss # Custom portfolio styles
├── _layouts/
│   ├── home.html            # Homepage layout
│   └── project.html         # Project detail layout
├── _projects/               # Project collection
│   ├── ai-code-review.md
│   ├── ecommerce-platform.md
│   └── task-management-app.md
├── _posts/                  # Blog posts
│   ├── 2023-12-15-scalable-react-architecture.md
│   └── 2024-01-10-modern-javascript-es2024-features.md
├── index.md                 # Homepage
├── about.md                 # About page
├── resume.md                # Resume page
├── projects.md              # Projects overview
├── blog.md                  # Blog overview
├── timeline.md              # Timeline overview
└── contact.md               # Contact page
```

## Setup

### Prerequisites

- Ruby 2.7+ and Bundler
- Git
- GitHub account (for GitHub Pages deployment)

### Local Development

1. **Clone the repository**:
   ```bash
   git clone <your-repo-url>
   cd portfolio-site
   ```

2. **Install dependencies**:
   ```bash
   bundle install
   ```

3. **Start the development server**:
   ```bash
   bundle exec jekyll serve
   ```

4. **Open in browser**:
   Navigate to `http://localhost:4000`

### GitHub Pages Deployment

1. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "Initial portfolio setup"
   git push origin main
   ```

2. **Enable GitHub Pages**:
   - Go to your repository settings
   - Scroll to "Pages" section
   - Select "Deploy from a branch"
   - Choose "main" branch and "/ (root)" folder
   - Save

3. **Custom Domain (Optional)**:
   - Add a `CNAME` file with your domain
   - Configure DNS records
   - Update `_config.yml` with your domain

## Customization

### Personal Information

1. **Update `_config.yml`**:
   - Change `title`, `description`, and `author`
   - Update social media links
   - Modify contact information

2. **Replace sample content**:
   - Update `about.md` with your story
   - Modify `resume.md` with your experience
   - Update `contact.md` with your details

### Adding Content

#### Projects

Create new files in `_projects/` with this format:

```markdown
---
title: "Project Name"
description: "Brief description"
date: 2023-01-01
technologies: ["React", "Node.js", "PostgreSQL"]
github_url: "https://github.com/username/project"
live_url: "https://project-demo.com"
featured: true
timeline:
  show: true
  category: "project"
  milestone: "Launch"
  impact: "Specific impact or achievement"
---

Project details with IDE syntax highlighting...
```

#### Blog Posts

Create new files in `_posts/` with this format:

```markdown
---
title: "Post Title"
date: 2023-01-01
categories: [tutorial, javascript]
tags: [react, hooks, frontend]
timeline:
  show: true
  category: "article"
  milestone: "Technical Article"
  impact: "Engagement metrics or recognition"
---

Post content with syntax highlighting...
```

### Timeline Integration

The timeline page automatically pulls from your projects and blog posts. To include an item in the timeline, add the following to the front matter:

```yaml
timeline:
  show: true                    # Set to true to include in timeline
  category: "project"           # "project" or "article"
  milestone: "Launch"           # Brief milestone description
  impact: "Description"         # Impact or achievement (optional)
```

#### Timeline Categories

- **Projects**: Automatically pulls from `_projects/` collection
- **Articles**: Automatically pulls from `_posts/` collection
- **Automatic Sorting**: Items are sorted by date (newest first)
- **Impact Tracking**: Optional impact metrics for each milestone

### Styling

#### IDE Syntax Highlighting

The portfolio uses custom IDE-style syntax highlighting. Use these classes in your content:

- `.ide-keyword` - for keywords (blue)
- `.ide-string` - for strings (green)
- `.ide-comment` - for comments (gray)
- `.ide-function` - for functions (yellow)
- `.ide-variable` - for variables (light blue)
- `.ide-operator` - for operators (white)
- `.ide-bracket` - for brackets (white)
- `.ide-property` - for properties (red)
- `.ide-class` - for classes (cyan)

Example:
```html
<span class="ide-keyword">const</span> <span class="ide-variable">myVar</span> <span class="ide-operator">=</span> <span class="ide-string">"Hello World"</span><span class="ide-operator">;</span>
```

#### Custom Styling

Modify `_sass/_portfolio-custom.scss` to customize:
- Colors and themes
- Layout and spacing
- Component styles
- Responsive breakpoints

#### IDE Color Scheme

Update `_sass/_ide-syntax.scss` to change the color scheme:
- Modify CSS variables in the `:root` selector
- Based on VS Code Dark+ theme by default
- Easy to adapt to other IDE themes

### Configuration Options

Key `_config.yml` settings:

```yaml
# Site settings
title: "Your Name"
description: "Your tagline"
author: "Your Name"

# Theme
remote_theme: "b2a3e8/jekyll-theme-console"

# Collections
collections:
  projects:
    output: true
    permalink: /:collection/:name/

# Navigation
header_pages:
  - index.md
  - about.md
  - resume.md
  - projects.md
  - blog.md
  - timeline.md
  - contact.md
```

## Development Tips

### Local Testing

- Use `bundle exec jekyll serve --livereload` for auto-refresh
- Check `_site/` folder for generated files
- Use `bundle exec jekyll build` to build without serving

### Content Tips

- Use front matter for metadata
- Include proper `date` fields for sorting
- Use descriptive filenames
- Add alt text for images
- Include relevant tags and categories

### Performance

- Optimize images before adding
- Use proper markdown syntax
- Minimize custom CSS
- Test on mobile devices

## Troubleshooting

### Common Issues

1. **Ruby version conflicts**:
   - Use rbenv or RVM to manage Ruby versions
   - Ensure Ruby 2.7+ is installed

2. **Bundler issues**:
   - Run `bundle update` to update gems
   - Delete `Gemfile.lock` and run `bundle install`

3. **GitHub Pages deployment**:
   - Check repository settings
   - Ensure `_config.yml` is properly formatted
   - Review GitHub Pages build logs

4. **Styling issues**:
   - Check browser console for errors
   - Verify SCSS syntax in custom files
   - Clear browser cache

### Getting Help

- Check Jekyll documentation: https://jekyllrb.com/docs/
- GitHub Pages documentation: https://docs.github.com/en/pages
- Console theme documentation: https://github.com/b2a3e8/jekyll-theme-console

## License

This portfolio template is open source and available under the [MIT License](LICENSE).

## Contributing

Feel free to submit issues and pull requests to improve this portfolio template.

---

**Happy coding!** 🚀

---

*This portfolio showcases not just your projects, but your attention to detail and design sensibility. Make it uniquely yours!*
