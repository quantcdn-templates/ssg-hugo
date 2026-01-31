# Hugo Starter Template for QuantCDN

A minimal Hugo static site starter template configured for deployment to QuantCDN.

[![Deploy to QuantCDN](https://www.quantcdn.io/img/quant-deploy-btn-sml.svg)](https://dashboard.quantcdn.io/projects/add/jamstack/ssg-hugo)

## Features

- **Hugo** - Fast and flexible static site generator
- **Automated Deployment** - GitHub Actions workflow for CI/CD
- **Quant Integration** - Pre-configured for QuantCDN deployment
- **Modern Styling** - Clean, responsive design out of the box

## Quick Start

1. Clone this repository
2. Install Hugo: `brew install hugo` (macOS) or see [Hugo installation guide](https://gohugo.io/installation/)
3. Run locally: `hugo server -D`
4. Visit `http://localhost:1313`

## Project Structure

```
.
├── .github/
│   └── workflows/
│       └── deploy.yml       # Automated deployment workflow
├── archetypes/              # Content templates
├── content/                 # Your content (markdown files)
├── layouts/                 # HTML templates
├── static/                  # Static assets (images, CSS, JS)
├── config.toml             # Hugo configuration
└── README.md
```

## Deployment

This template includes a GitHub Actions workflow that automatically:
1. Builds your Hugo site on every push to `main`
2. Deploys the generated static files to QuantCDN
3. Purges the CDN cache for instant updates

### Environment Variables

The following are automatically configured by QuantCDN:
- `QUANT_CUSTOMER` - Your Quant customer ID (repository variable)
- `QUANT_PROJECT` - Your Quant project ID (repository variable)
- `QUANT_TOKEN` - Your Quant API token (secret)

## Customization

### Site Configuration

Edit `config.toml` to customize your site:

```toml
baseURL = "https://your-domain.com/"
languageCode = "en-us"
title = "My Hugo Site"
theme = "quant-minimal"
```

### Adding Content

Create new pages:
```bash
hugo new posts/my-first-post.md
```

### Styling

Add custom CSS in `static/css/custom.css` or modify the theme in `layouts/`.

## Learn More

- [Hugo Documentation](https://gohugo.io/documentation/)
- [Quant Documentation](https://docs.quantcdn.io/)
