## Development

When starting the dev server, use background mode:

```
astro dev --background
```

Manage the background server with `astro dev stop`, `astro dev status`, and `astro dev logs`.

## Package Management & Dependencies Rules

- **Package Manager**: Use `pnpm` exclusively.
- **Exact Versions**: All dependencies must be installed with exact versions. Do NOT use `^` (caret) or `~` (tilde).
  - Production dependency: `pnpm add -E <package>`
  - Development dependency: `pnpm add -E -D <package>`

## Project Structure

The project follows this basic structure:

- `src/models/`: TypeScript interfaces and domain type definitions.
- `src/mocks/`: Mock data and test fixtures.
- `src/components/`: Reusable UI components (Astro and React).
- `src/services/`: Data access and business logic services.
- `src/utils/`: Shared helper functions and utility libraries.
- `docs/`: Project documentation (`docs/index.md`).

## Documentation

Full documentation: https://docs.astro.build

Consult these guides before working on related tasks:

- [Adding pages, dynamic routes, or middleware](https://docs.astro.build/en/guides/routing/)
- [Working with Astro components](https://docs.astro.build/en/basics/astro-components/)
- [Using React, Vue, Svelte, or other framework components](https://docs.astro.build/en/guides/framework-components/)
- [Adding or managing content](https://docs.astro.build/en/guides/content-collections/)
- [Adding styles or using Tailwind](https://docs.astro.build/en/guides/styling/)
- [Supporting multiple languages](https://docs.astro.build/en/guides/internationalization/)
