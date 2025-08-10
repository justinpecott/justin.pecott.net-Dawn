# justin.pecott.net

A highly functional [Ghost](https://github.com/TryGhost/Ghost) theme that adapts to the reader's preferences. Let them read, search, subscribe, navigate, and more with ease.

Customized fork of [Dawn](https://github.com/TryGhost/Dawn)

## Auto-Deployment

This repository is configured with GitHub Actions to automatically deploy the theme to Ghost on every push to the `main` branch.

### Setup Required Secrets

To enable auto-deployment, configure these secrets in your GitHub repository (`Settings` → `Secrets and variables` → `Actions`):

- **`GHOST_ADMIN_API_URL`**: Your Ghost Admin API URL (found in Ghost Admin → Integrations)
- **`GHOST_ADMIN_API_KEY`**: Your Ghost Admin API Key (found in Ghost Admin → Integrations)

### How it Works

1. Push changes to the `main` branch
2. GitHub Actions automatically:
   - Installs dependencies
   - Builds theme assets
   - Deploys to your Ghost site using the [official TryGhost action](https://github.com/TryGhost/action-deploy-theme)

## Development

You'll need [Node](https://nodejs.org/) and [Yarn](https://yarnpkg.com/) installed. After that, from the project's root directory:

```bash
# Install dependencies
yarn install

# Validate theme
yarn test

# Build assets
yarn build

# Development with live reload
yarn dev

# Build and package theme for manual upload
yarn zip
```

### File Structure

- Edit CSS files in `assets/css/` - compiled to `assets/built/screen.css`
- Edit JS files in `assets/js/` - compiled to `assets/built/main.min.js`
- Theme templates are `.hbs` files in the root and `partials/` directory

### Manual Installation

To create an installable theme zip file:

```bash
yarn zip
```

Upload the generated `dist/justin-pecott-net.zip` file to Ghost Admin → Design → Change theme.
