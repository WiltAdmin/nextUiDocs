Requirements:

___

[![Sponsored: MongoDB](https://media.ethicalads.io/media/images/2023/07/mongodb-codedark-240x180.png)](https://server.ethicalads.io/proxy/click/5092/78b64b98-2d3c-49f4-b189-4bf112e2f433/)

To use NextUI in your Astro project, you need to follow the following steps:

### [Installation](https://nextui.org/docs/frameworks/astro#installation)

In your Astro project, run one of the following command to install NextUI:

```
npm i @nextui-org/react framer-motion
```

### [Tailwind CSS Setup](https://nextui.org/docs/frameworks/astro#tailwind-css-setup)

NextUI is built on top of Tailwind CSS, so you need to install Tailwind CSS first. You can follow the official [installation guide](https://tailwindcss.com/docs/guides/astro) to install Tailwind CSS. Then you need to add the following code to your `tailwind.config.cjs` file:

```
// tailwind.config.cjsconst { nextui } = require("@nextui-org/react");/** @type {import('tailwindcss').Config} */module.exports = {  content: [    // ...    './node_modules/@nextui-org/theme/dist/**/*.{js,ts,jsx,tsx}'  ],  theme: {    extend: {},  },  darkMode: "class",  plugins: [nextui()]}
```

### [Usage](https://nextui.org/docs/frameworks/astro#usage)

Now you can import NextUI components and use them in your Astro project:

```
---import Layout from '../layouts/Layout.astro';import {Button} from '@nextui-org/react';---<Layout title="Welcome to Astro.">  <main>      <Button color="primary" client:visible>My button</Button>  </main></Layout>
```

Note that you have to add `client:visible` to the component to make it visible only on the client side. Otherwise some functionalities of NextUI components may not work properly.

### [Setup pnpm (optional)](https://nextui.org/docs/frameworks/astro#setup-pnpm-optional)

If you are using pnpm, you need to add the following code to your `.npmrc` file:

```
public-hoist-pattern[]=*@nextui-org/theme*
```

After modfiying the `.npmrc` file, you need to run `pnpm install` again to ensure that the dependencies are installed correctly.

> Version 2 is only compatible with React 18 or later. If you are using React 17 or earlier, please use [version 1 of NextUI](https://v1.nextui.org/docs/getting-started).