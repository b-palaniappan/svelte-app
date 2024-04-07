# create-svelte

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/main/packages/create-svelte).

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npm create svelte@latest

# create a new project in my-app
npm create svelte@latest my-app
```

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.

## Project docs

### Adding shadcn components

- To add a new shadcn compoent, run `pnpm dlx shadcn-svelte@latest add <compoent-name>`. Example: `pnpm dlx shadcn-svelte@latest add Button`.
- To update shadcn components, run `pnpm dlx shadcn-svelte@latest update`. This will update all shadcn components to the latest version.

### Adding fonts

- To add a new font from [fontsource](https://fontsource.org/), run `pnpm add @fontsource/poppins`.
- Then import the font in `src/app.pcss` like this: `import '@fontsource/poppins';`.
- Then add it to the css as, under `@layer base`.

```css
@font-face {
	font-family: 'Poppins', sans-serif;
	font-display: swap;
}
```
