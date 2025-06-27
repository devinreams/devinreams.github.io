# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based personal website/blog hosted on GitHub Pages. The site includes:
- Personal blog posts (markdown files in `_posts/`)
- Static pages (like `/about/`)
- Both standard posts and link posts
- Social media integration (Twitter, Facebook Open Graph)
- RSS/Atom feed generation

## Architecture

### Key Directories
- `_posts/` - Blog posts in markdown format with YAML frontmatter
- `_layouts/` - Jekyll layout templates (default.html, post.html, page.html, link.html)
- `_includes/` - Reusable template partials (head.html, foot.html)
- `_drafts/` - Unpublished draft posts
- `css/` - Stylesheets including compiled LESS
- `img/` - Image assets organized by year
- `about/` - Static about page

### Template Structure
- `default.html` - Base layout with header, navigation, and footer
- `post.html` - Blog post layout extending default
- `page.html` - Static page layout extending default  
- `link.html` - Special layout for link posts extending default

### Key Features
- Jekyll plugins: mentions, emoji, redirects, sitemap, feed, pagination
- Security headers (CSP, XSS protection, frame options)
- Social media meta tags for Twitter cards and Facebook Open Graph
- Custom CSS with version cache busting
- Octicons for icons
- Google Analytics integration
- "Improve this page" GitHub edit links

## Development Commands

### Local Development
```bash
# Install dependencies (if Jekyll/bundler not installed)
gem install jekyll bundler

# Serve locally with auto-regeneration
jekyll serve

# Build for production
jekyll build
```

### Deployment
The site is automatically deployed via GitHub Pages when changes are pushed to the main branch. No manual deployment is needed.

## Content Guidelines

### Blog Posts
- Use YAML frontmatter with title, date, and optional layout
- Default layout is "post" 
- For link posts, use layout "link" and include a "link" field in frontmatter
- Images should be placed in `/img/YYYY/` folders organized by year
- Posts should use markdown format with `.md` extension

### Styling
- Main styles are in `/css/styles.css` 
- LESS source is in `/css/styles.less`
- Theme uses "theme-base-08" color scheme
- Responsive design with mobile-first approach