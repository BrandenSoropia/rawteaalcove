

## Developing

**Requirements:**
- [Node version manager "n"](https://github.com/tj/n)
  - Repo contains `.node-version` to hopefully make it easier for multiple different node version managers to recognize and install.
  - As a bonus, `.node-version` seems to be readable by Cloudflare which I intend to use as my host. [Read more about this file here](https://github.com/shadowspawn/node-version-usage)
- Node `v16.16.0`

**Technology used:**
- Svelte

### Running locally

1. Install dependencies: `npm install`
2. Run local server and open the app in a new browser tab: `npm run dev -- --open`
  - The app will be served from `localhost:5173`

## Building (Stuff from Sveltekit README)

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.

## Deploying to Cloudflare

Follow these steps: https://developers.cloudflare.com/pages/framework-guides/deploy-a-svelte-site