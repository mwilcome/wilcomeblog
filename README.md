# Mike Wilcome's Blog

Welcome to my personal blog! I’m Mike Wilcome, a Principal Engineer with over a decade of experience in full-stack Java development, microservices, and leadership in fintech and healthcare. This site showcases my career journey, projects, and insights into software engineering. It’s built with Hugo, hosted on Netlify, and accessible at [mikewilcome.info](https://mikewilcome.info).

## Project Overview

This blog is a static site generated with Hugo, using the PaperMod theme for a clean, modern look. It’s hosted on Netlify, with automatic deployments triggered by pushes to the GitHub repository. The custom domain `mikewilcome.info` is configured via Namecheap DNS.

### Features
- **Homepage**: A welcoming page with my profile picture and a brief intro.
- **About Page**: Details my education, career highlights, and contact info.
- **Blog**: A collection of posts about my projects and tech experiences.
- **Responsive Design**: Works seamlessly on desktop and mobile.

## Project Structure

The project follows a standard Hugo structure, with all files in the root directory:

```
wilcomeblog/
├── archetypes/       # Templates for new content
├── assets/           # Processed assets (e.g., images for profile)
├── content/          # Blog posts and pages
│   ├── blog/         # Blog post Markdown files
│   ├── _index.md     # Homepage content
│   └── about.md      # About page content
├── layouts/          # Custom templates (if any)
├── public/           # Generated static site (ignored by Git)
├── static/           # Static assets (e.g., images)
│   └── images/       # Image files like IMG_7839.JPG
├── .gitignore        # Git ignore file
├── go.mod            # Go module file for Hugo dependencies
├── go.sum            # Go module checksums
├── hugo.toml         # Site configuration
└── README.md         # This file
```

## Prerequisites

To work on this site locally, you’ll need:
- **Hugo**: Version 0.145.0 (extended edition). Install via [Hugo releases](https://github.com/gohugoio/hugo/releases) or a package manager (e.g., `brew install hugo` on macOS).
- **Git**: For version control and pushing to GitHub.
- **Node.js**: Optional, for managing any theme dependencies (not currently required for PaperMod).
- **Netlify CLI**: Optional, for local Netlify testing (`npm install -g netlify-cli`).

## Setup Instructions

### Local Setup
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/mwilcome/wilcomeblog.git
   cd wilcomeblog
   ```

2. **Install Hugo**:
    - Ensure Hugo 0.145.0 is installed:
      ```bash
      hugo version
      ```
    - If not, install it (e.g., `brew install hugo` on macOS).

3. **Run Locally**:
    - Start the Hugo development server:
      ```bash
      hugo server
      ```
    - Open your browser to `http://localhost:1313` to preview the site.

### Adding Content
- **New Blog Post**: Create a new post in the `content/blog/` directory:
  ```bash
  hugo new blog/my-new-post.md
  ```
  Edit `content/blog/my-new-post.md` with your content.

- **Update Pages**: Edit files like `content/_index.md` (homepage) or `content/about.md` directly.

### Building the Site
- Generate the static site into the `public/` folder:
  ```bash
  hugo
  ```

## Deployment

This site is hosted on Netlify with automatic deployments from the GitHub repository.

### Netlify Configuration
- **Repository**: [github.com/mwilcome/wilcomeblog](https://github.com/mwilcome/wilcomeblog)
- **Build Settings**:
    - **Base directory**: (blank, since Hugo files are in the root)
    - **Build command**: `hugo`
    - **Publish directory**: `public`
- **Environment Variables** (in `netlify.toml`):
  ```toml
  [build]
    command = "hugo"
    publish = "public"

  [build.environment]
    HUGO_VERSION = "0.145.0"
    GO_VERSION = "1.24.1"
  ```

### Deployment Workflow
1. **Make Changes**: Add or edit content (e.g., a new blog post).
2. **Build Locally** (optional but recommended):
   ```bash
   hugo
   ```
3. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "Added new blog post"
   git push origin main
   ```
4. **Netlify Deploy**: Netlify automatically detects the push, runs `hugo`, and deploys the site from the `public/` folder.

## Domain Configuration
- **Custom Domain**: `mikewilcome.info`
- **DNS Setup** (via Namecheap):
    - **A Record**:
        - Host: `@`
        - Value: `104.198.14.52` (Netlify’s load balancer IP)
    - **CNAME Record**:
        - Host: `www`
        - Value: `wilcomeblog.netlify.app`
- Netlify handles HTTPS automatically once DNS propagates.

## Troubleshooting
- **Links Not Working**: Ensure menu URLs in `hugo.toml` use relative paths (e.g., `/about/`).
- **Build Fails**: Verify `HUGO_VERSION` and `GO_VERSION` match your local setup in Netlify’s settings.
- **Domain Issues**: Check DNS propagation with [dnschecker.org](https://dnschecker.org) if `mikewilcome.info` doesn’t resolve.

## Contributing
This is my personal blog, but feel free to fork it or suggest improvements via GitHub issues or pull requests!

## Contact
- **Email**: mike@mikewilcome.info
- **LinkedIn**: [linkedin.com/in/michael-wilcome-36377bb0](https://linkedin.com/in/michael-wilcome-36377bb0)
- **GitHub**: [github.com/mwilcome](https://github.com/mwilcome)