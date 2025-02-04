# Delicious Diaries - Gatsby and Ghost Site

&nbsp;

**Home Page**

<img width="1470" alt="home page" src="https://github.com/DulyaDeCosta/Delicious-diaries/assets/148673241/6a9bdc59-fa9a-436a-91c0-28438c7bd3cb">

&nbsp;

**About Page**

<img width="1470" alt="about page" src="https://github.com/DulyaDeCosta/Delicious-diaries/assets/148673241/31b6ba93-ffda-4620-b9ba-5e36f6182090">

&nbsp;

**Blog Post**

<img width="1470" alt="lunch blog" src="https://github.com/DulyaDeCosta/Delicious-diaries/assets/148673241/5e74c51b-edd0-4eec-a773-4f56a9c12b55">

<img width="1470" alt="lunch blog2" src="https://github.com/DulyaDeCosta/Delicious-diaries/assets/148673241/a1e3bc92-d85a-4f40-bb75-58451a1ca5f7">

&nbsp;

# Gatsby and Ghost Starter 

A starter template to build lightning fast websites with [Ghost](https://ghost.org/) & [Gatsby](https://gatsbyjs.org)

**Demo:** https://gatsby.ghost.org/


# Installing

```bash
# With Gatsby CLI
gatsby new gatsby-starter-ghost https://github.com/TryGhost/gatsby-starter-ghost.git
```

```bash
# From Source
git clone https://github.com/TryGhost/gatsby-starter-ghost.git
cd gatsby-starter-ghost
```

Then install dependencies

```bash
yarn
```

&nbsp;

# Running

Start the development server. You now have a Gatsby site pulling content from headless Ghost.

```bash
gatsby develop
```

By default, the starter will populate content from a default Ghost install located at https://gatsby.ghost.io.

To use your own install, you will need to edit the `.ghost.json` config file with your credentials. Change the `apiUrl` value to the URL of your Ghost site. For Ghost(Pro) customers, this is the Ghost URL ending in `.ghost.io`, and for people using the self-hosted version of Ghost, it's the same URL used to access your site.

Next, update the `contentApiKey` value to a key associated with the Ghost site. A key can be provided by creating an integration within Ghost Admin. Navigate to Integrations and click "Add new integration". Name the integration appropriately and click create.

Finally, configure your desired URL in `siteConfig.js`, so links (e. g. canonical links) are generated correctly. You can also update other default values, such as `postsPerPage` in this file.

To use this starter without issues, your Ghost installation needs to be at least on version `2.10.0`.

The default Ghost version that is used for this starter is `5.x`. If your Ghost installation is on a lower version, you will need to pass in a `version` property in your `.ghost.json` settings:

**Ghost >=2.10.0 <5.0.0**
```json
{
    "apiUrl": "https://gatsby.ghost.io",
    "contentApiKey": "9cc5c67c358edfdd81455149d0",
    "version": "v4.0"
}
```

**Ghost >=5.0.0**
```json
{
    "apiUrl": "https://gatsby.ghost.io",
    "contentApiKey": "9cc5c67c358edfdd81455149d0"
}
```

&nbsp;

# Deploying with Netlify

The starter contains three config files specifically for deploying with Netlify. A `netlify.toml` file for build settings, a `/static/_headers` file with default security headers set for all routes, and `/static/_redirects` to set Netlify custom domain redirects.

To deploy to your Netlify account, hit the button below.

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/TryGhost/gatsby-starter-ghost)

Content API Keys are generally not considered to be sensitive information, they exist so that they can be changed in the event of abuse; so most people commit it directly to their `.ghost.json` config file. If you prefer to keep this information out of your repository you can remove this config and set [Netlify ENV variables](https://www.netlify.com/docs/continuous-deployment/#build-environment-variables) for production builds instead.

Once deployed, you can set up a [Ghost + Netlify Integration](https://ghost.org/integrations/netlify/) to use deploy hooks from Ghost to trigger Netlify rebuilds. That way, any time data changes in Ghost, your site will rebuild on Netlify.

&nbsp;

# Optimising

You can disable the default Ghost Handlebars Theme front-end by enabling the `Make this site private` flag within your Ghost settings. This enables password protection in front of the Ghost install and sets `<meta name="robots" content="noindex" />` so your Gatsby front-end becomes the source of truth for SEO.

&nbsp;

# Extra options

```bash
# Run a production build, locally
gatsby build

# Serve a production build, locally
gatsby serve
```

Gatsby `develop` uses the `development` config in `.ghost.json` - while Gatsby `build` uses the `production` config.

&nbsp;

# Copyright & License

Copyright (c) 2013-2023 Ghost Foundation - Released under the [MIT license](LICENSE).
