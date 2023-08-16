### [Installation](https://nextui.org/docs/frameworks/remix#installation)

In your Remix project, run one of the following command to install NextUI:

```
npm i @nextui-org/react framer-motion
```

### [Tailwind CSS Setup](https://nextui.org/docs/frameworks/remix#tailwind-css-setup)

NextUI is built on top of Tailwind CSS, so you need to install Tailwind CSS first. You can follow the official [installation guide](https://tailwindcss.com/docs/guides/remix) to install Tailwind CSS. Then you need to add the following code to your `tailwind.config.js` file:

```
// tailwind.config.tsconst { nextui } = require("@nextui-org/react");import type { Config} from 'tailwindcss'export default {  content: [    // ...    './node_modules/@nextui-org/theme/dist/**/*.{js,ts,jsx,tsx}'  ],  theme: {    extend: {},  },  darkMode: "class",  plugins: [nextui()]} satisfies Config
```

### [Provider Setup](https://nextui.org/docs/frameworks/remix#provider-setup)

After installing NextUI, you need to set up the `NextUIProvider` at the `root` of your application.

Go to the src directory and inside `root.tsx`, wrap `NextUIProvider` around App:

```
import {  Links,  LiveReload,  Meta,  Outlet,  Scripts,  ScrollRestoration,} from "@remix-run/react";import {NextUIProvider} from "@nextui-org/react";export default function App() {  return (    <html lang="en">      <head>        <Meta />        <Links />      </head>      <body>        <NextUIProvider>          <Outlet />          <ScrollRestoration />          <Scripts />          <LiveReload />        </NextUIProvider>      </body>    </html>  );}
```

### [Setup pnpm (optional)](https://nextui.org/docs/frameworks/remix#setup-pnpm-optional)

If you are using pnpm, you need to add the following code to your `.npmrc` file:

```
public-hoist-pattern[]=*@nextui-org/theme*
```

After modfiying the `.npmrc` file, you need to run `pnpm install` again to ensure that the dependencies are installed correctly.