# create-svelte

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte).

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

---

# Svelte + Vite

This template should help get you started developing with Svelte in Vite.

## Recommended IDE Setup

[VS Code](https://code.visualstudio.com/) + [Svelte](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode).

## Need an official Svelte framework?

Check out [SvelteKit](https://github.com/sveltejs/kit#readme), which is also powered by Vite. Deploy anywhere with its serverless-first approach and adapt to various platforms, with out of the box support for TypeScript, SCSS, and Less, and easily-added support for mdsvex, GraphQL, PostCSS, Tailwind CSS, and more.

## Technical considerations

**Why use this over SvelteKit?**

- It brings its own routing solution which might not be preferable for some users.
- It is first and foremost a framework that just happens to use Vite under the hood, not a Vite app.

This template contains as little as possible to get started with Vite + Svelte, while taking into account the developer experience with regards to HMR and intellisense. It demonstrates capabilities on par with the other `create-vite` templates and is a good starting point for beginners dipping their toes into a Vite + Svelte project.

Should you later need the extended capabilities and extensibility provided by SvelteKit, the template has been structured similarly to SvelteKit so that it is easy to migrate.

**Why `global.d.ts` instead of `compilerOptions.types` inside `jsconfig.json` or `tsconfig.json`?**

Setting `compilerOptions.types` shuts out all other types not explicitly listed in the configuration. Using triple-slash references keeps the default TypeScript setting of accepting type information from the entire workspace, while also adding `svelte` and `vite/client` type information.

**Why include `.vscode/extensions.json`?**

Other templates indirectly recommend extensions via the README, but this file allows VS Code to prompt the user to install the recommended extension upon opening the project.

**Why enable `checkJs` in the JS template?**

It is likely that most cases of changing variable types in runtime are likely to be accidental, rather than deliberate. This provides advanced typechecking out of the box. Should you like to take advantage of the dynamically-typed nature of JavaScript, it is trivial to change the configuration.

**Why is HMR not preserving my local component state?**

HMR state preservation comes with a number of gotchas! It has been disabled by default in both `svelte-hmr` and `@sveltejs/vite-plugin-svelte` due to its often surprising behavior. You can read the details [here](https://github.com/rixo/svelte-hmr#svelte-hmr).

If you have state that's important to retain within a component, consider creating an external store which would not be replaced by HMR.

```js
// store.js
// An extremely simple external store
import { writable } from 'svelte/store'
export default writable(0)
```

---

# Here is a response from ChatGPT when comparing SvelteKit with Svelte + Vite

> SvelteKit is a framework built on top of Svelte that aims to provide a more opinionated and streamlined way of building web applications. It includes features like server-side rendering, routing, and API endpoints out of the box, along with a set of conventions and helpers to make building web apps faster and easier.
>
> On the other hand, Svelte with Vite is a more lightweight and customizable approach that allows you to build web applications using Svelte as the front-end framework and Vite as the build tool. Vite is a modern build tool that focuses on fast development and supports hot module replacement, code splitting, and other modern features out of the box.
>
> The key difference between SvelteKit and Svelte with Vite is the level of abstraction and convenience provided by each approach. SvelteKit provides a more opinionated way of building web applications that aims to reduce the amount of boilerplate and configuration needed to get started, while Svelte with Vite gives you more flexibility and control over how you build your app.
>
> In terms of features, SvelteKit includes built-in support for server-side rendering, routing, and API endpoints, while Svelte with Vite requires you to set up these features manually or using third-party libraries. However, Svelte with Vite allows you to use any build tool or server framework you prefer, while SvelteKit has a more tightly integrated stack.
>
> Ultimately, the choice between SvelteKit and Svelte with Vite depends on your specific needs and preferences. If you value convenience and are building a more complex web application that requires server-side rendering and API endpoints, SvelteKit may be the better choice. If you prefer more flexibility and control over your build process, Svelte with Vite may be a better fit.
