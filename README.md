# Hugo Starter Template for QuantCDN

A minimal Hugo static site starter template configured for deployment to QuantCDN.

[![Deploy to QuantCDN](https://www.quantcdn.io/img/quant-deploy-btn-sml.svg)](https://dashboard.quantcdn.io/deploy/static/ssg-hugo)

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
│       ├── ci.yml            # CI build validation workflow
│       └── deploy.yml        # Automated deployment workflow
├── content/                  # Your content (markdown files)
├── layouts/                  # HTML templates
├── quant/
│   └── meta.json             # Quant template metadata
├── config.toml               # Hugo configuration
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
```

### Adding Content

Create new pages:
```bash
hugo new posts/my-first-post.md
```

### Styling

Modify the inline styles in `layouts/index.html` or add a `static/css/` directory for external stylesheets.

## Learn More

- [Hugo Documentation](https://gohugo.io/documentation/)
- [Quant Documentation](https://docs.quantcdn.io/)
