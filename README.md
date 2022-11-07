# Next.js 13 + Turbopack App

This is the base for my personal website currently using turbopack alpha.

**Turbopack is currently in alpha and not yet ready for production**

## Running Locally

1. Install dependencies: `yarn`
1. Start the dev server: `yarn dev`

**Note:** The playground uses [Tailwind CSS](https://tailwindcss.com). However, Turbopack does not yet support fully [PostCSS](https://turbo.build/pack/docs/features/css#postcss), but it does support CSS and CSS Modules. [As a workaround](https://turbo.build/pack/docs/features/css#tailwind-css), we run Tailwind through it's CLI upon `postinstall`. For live reload of CSS, you can run Tailwind in another process with the `--watch` flag or install `concurrently` and modify your `dev` script:

```bash
yarn add concurrently --dev
```

Then modify your `dev` script in `package.json`:

```json
{
  "scripts": {
    "dev": "concurrently \"next dev --turbo\" \"npm run tailwind --watch\""
  }
}
```

For more information, see: https://turbo.build/pack/docs/features/css#tailwind-css