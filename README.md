# Cloudflare Next.js Quickstart

This project is a quickstart for starting a Next.js to deploy on Cloudflare Pages.

The quickstart includes some defaults for:

- Basic Next.js setup with [Tailwind CSS](https://tailwindcss.com/)
- Deployments to Cloudflare via [GitHub Actions](.github/workflows)
- Formatting and linting via [Biome](https://biomejs.dev/)

For a more complete using pnpm workspaces and a monorepo with a [Hono](https://hono.dev) API deployed to Cloudflare Workers, check out our [cloudflare-quickstart](https://github.com/gmdotdev/cloudflare-quickstart).

## Getting Started

1. Clone this repository

```bash
  git clone git@github.com:gmdotdev/cloudflare-nextjs-quickstart.git
```

2. Install dependencies

```bash
  pnpm install
```

3. Start the development server

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Deploying to Cloudflare

1. Create a new GitHub repository for your project.

2. Set up the following GitHub repository secrets:

- [`CLOUDFLARE_ACCOUNT_ID`](https://developers.cloudflare.com/fundamentals/setup/find-account-and-zone-ids/)
- [`CLOUDFLARE_API_TOKEN`](https://developers.cloudflare.com/workers/wrangler/ci-cd/#api-token)

3. Create the Cloudflare Pages app with a project name matching that in [build-and-deploy.yml](.github/workflows/build-and-deploy.yml). You can create a new Pages app by:

- Go to Workers & Pages in Cloudflare
- Click the Pages tab and then `Upload assets`
- Type the project name and click `Create Project`, skip the rest

4. Push your repository to GitHub. The GitHub Actions workflow is set to manual trigger by default, so navigate to Actions to run the deploys manually.

### Using Custom Domains

To use a custom domain with Cloudflare Pages, you can follow the [official documentation](https://developers.cloudflare.com/pages/configuration/custom-domains/).

**Note**: This assumes your domain is already set up in Cloudflare.

## Links

- [Biome](https://biomejs.dev/)
- [Cloudflare next-on-pages](https://developers.cloudflare.com/pages/framework-guides/nextjs/deploy-a-nextjs-site/)
- [Next.js](https://nextjs.org)
