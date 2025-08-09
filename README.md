# justin.pecott.net-Dawn

A highly functional [Ghost](https://github.com/TryGhost/Ghost) theme that adapts to the reader's preferences. Let them read, search, subscribe, navigate, and more with ease.

Customized fork of [Dawn](https://github.com/TryGhost/Dawn)

## Development

You'll need [Node](https://nodejs.org/), [Yarn](https://yarnpkg.com/) and [Gulp](https://gulpjs.com) installed globally. After that, from the project's root directory:

```bash
# install dependencies
yarn

# run development server
yarn dev
```

Now you can edit files in `packages/<theme-name>/assets/css/` or `packages/<theme-name>/assets/js/`, which will be compiled to `packages/<theme-name>/assets/built/` automatically.

To run a theme locally, you need to symlink a theme to your local Ghost site.

```bash
# run a theme locally
yarn symlink --theme <theme-name> --site /dir/to/your/ghost-site
```

Or if you're running a Ghost instance via the CLI:

```bash
yarn symlink --theme <theme-name> --site /dir/to/ghost-instance
```

Restart your Ghost instance and the theme will be listed in the `Design` settings.

To create an installable theme zip file in `packages/<theme-name>/dist/`:

```bash
# create .zip file
yarn zip --theme <theme-name>
```
