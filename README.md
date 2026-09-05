# Handy Acosta Cuellar Portfolio

Personal academic portfolio for Handy Acosta Cuellar, Ph.D., built with Astro and Tailwind CSS. The site presents research, teaching, public scholarship, and contact information in English and Spanish.

## Stack

- [Astro](https://astro.build/) for pages and components
- [Tailwind CSS](https://tailwindcss.com/) v4 through the Vite plugin
- [Vercel adapter](https://docs.astro.build/en/guides/integrations-guide/vercel/) for deployment
- `pnpm` for package management

## Project structure

```text
/
├── public/                 # Static files and favicons
├── src/
│   ├── assets/             # Imported Astro assets
│   ├── components/
│   │   ├── Section.astro   # Shared section wrapper
│   │   └── Sections/       # Home page sections
│   ├── layouts/Layout.astro
│   ├── pages/               # English and Spanish routes
│   └── styles/global.css    # Tailwind theme and shared component recipes
├── astro.config.mjs
└── package.json
```

## Routes

- `/` — English home
- `/research/` — Research and publications
- `/teaching/` — Teaching and courses
- `/es/` — Spanish home
- `/es/research/` — Investigación
- `/es/teaching/` — Docencia y pedagogía

## Development

Install dependencies:

```sh
pnpm install
```

Start the local server:

```sh
pnpm dev
```

The site is available at `http://localhost:4321`.

Build for production:

```sh
pnpm build
```

Preview the production build:

```sh
pnpm preview
```

## Styling with Tailwind

Shared design tokens are defined in `src/styles/global.css` inside `@theme`, including colors and font families. Existing component recipes use Tailwind's `@apply`, while page-specific markup can use utility classes directly:

```astro
<div class="grid gap-6 bg-cream p-8 md:grid-cols-2">
  ...
</div>
```

Prefer Tailwind utilities in new markup. Add a reusable recipe to the `@layer components` block only when the same combination is used in several components.

## Content notes

The current content was migrated from the public WordPress site. External documents and publication links remain external. The contact email should be confirmed before the site is published.
