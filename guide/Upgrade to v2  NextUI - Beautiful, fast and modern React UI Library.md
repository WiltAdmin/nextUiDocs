Requirements:

___

[![Sponsored: Browserless](https://media.ethicalads.io/media/images/2023/02/Browserless_Ad_Feb_2023.png)](https://server.ethicalads.io/proxy/click/5152/d4ca527a-556d-4b4e-8e5a-6de72f3cf195/)

## [Next.js upgrade steps](https://nextui.org/docs/guide/upgrade-to-v2#nextjs-upgrade-steps)

Make sure to follow the previous steps since they are required to upgrade to v2.

## [App directory Setup](https://nextui.org/docs/guide/upgrade-to-v2#app-directory-setup)

Next.js 13 introduces a new `app/` directory structure. By default it uses Server Components. As NextUI components use React hooks, we added the `use client;` at build time, so you can import them directly in your React Server Components (RSC).

### [Installation](https://nextui.org/docs/guide/upgrade-to-v2#installation)

In your Next.js project, run one of the following command to install NextUI:

```
npm i @nextui-org/react framer-motion
```

### [Tailwind CSS Setup](https://nextui.org/docs/guide/upgrade-to-v2#tailwind-css-setup)

NextUI is built on top of Tailwind CSS, so you need to install Tailwind CSS first. You can follow the official [installation guide](https://tailwindcss.com/docs/guides/nextjs) to install Tailwind CSS. Then you need to add the following code to your `tailwind.config.js` file:

```
// tailwind.config.jsconst { nextui } = require("@nextui-org/react");/** @type {import('tailwindcss').Config} */module.exports = {  content: [    // ...    './node_modules/@nextui-org/theme/dist/**/*.{js,ts,jsx,tsx}'  ],  theme: {    extend: {},  },  darkMode: "class",  plugins: [nextui()]}
```

### [Setup Provider](https://nextui.org/docs/guide/upgrade-to-v2#setup-provider)

Go to your `app/providers.tsx` or `app/providers.jsx` (create it if it doesn't exist) and wrap the Component with the `NextUIProvider`:

```
// app/providers.tsx'use client'import {NextUIProvider} from '@nextui-org/react'export function Providers({children}: { children: React.ReactNode }) {  return (    <NextUIProvider>      {children}    </NextUIProvider>  )}
```

### [Add Provider to Root](https://nextui.org/docs/guide/upgrade-to-v2#add-provider-to-root)

Now, Go to your `root` layout page and wrap it with the `NextUIProvider`:

```
// app/layout.tsximport {Providers} from "./providers";export default function RootLayout({children}: { children: React.ReactNode }) {  return (    <html lang="en" className='dark'>      <body>        <Providers>          {children}        </Providers>      </body>    </html>  );}
```

> **Note**: NextUI automatically add two themes `light` and `dark` to your application. You can use any of them by adding the `dark`/`light` class to the `html` tag. See the [theme docs](https://nextui.org/docs/customization/customize-theme) for more details.

### [Use NextUI Components](https://nextui.org/docs/guide/upgrade-to-v2#use-nextui-components)

Now you can import any NextUI component directly in your Server Components without needing to use the `use client;` directive:

```
// app/page.tsximport {Button} from '@nextui-org/button'export default function Page() {  return (    <div>      <Button>Click me</Button>    </div>  )}
```

> **Important 🚨**: Note that you need to import the component from the individual package, not the from `@nextui-org/react`.

### [Setup pnpm (optional)](https://nextui.org/docs/guide/upgrade-to-v2#setup-pnpm-optional)

If you are using pnpm, you need to add the following code to your `.npmrc` file:

```
public-hoist-pattern[]=*@nextui-org/theme*
```

After modfiying the `.npmrc` file, you need to run `pnpm install` again to ensure that the dependencies are installed correctly.

## [Pages Directory Setup](https://nextui.org/docs/guide/upgrade-to-v2#pages-directory-setup)

### [Installation](https://nextui.org/docs/guide/upgrade-to-v2#installation-1)

In your Next.js project, run one of the following command to install NextUI:

```
npm i @nextui-org/react framer-motion
```

### [Tailwind CSS Setup](https://nextui.org/docs/guide/upgrade-to-v2#tailwind-css-setup-1)

NextUI is built on top of Tailwind CSS, so you need to install Tailwind CSS first. You can follow the official [installation guide](https://tailwindcss.com/docs/guides/nextjs) to install Tailwind CSS. Then you need to add the following code to your `tailwind.config.js` file:

```
// tailwind.config.jsconst { nextui } = require("@nextui-org/react");/** @type {import('tailwindcss').Config} */module.exports = {  content: [    // ...    './node_modules/@nextui-org/theme/dist/**/*.{js,ts,jsx,tsx}'  ],  theme: {    extend: {},  },  darkMode: "class",  plugins: [nextui()]}
```

### [Setup Provider](https://nextui.org/docs/guide/upgrade-to-v2#setup-provider-1)

Go to pages`/_app.js` or `pages/_app.tsx` (create it if it doesn't exist) and wrap the Component with the `NextUIProvider`:

```
// pages/_app.jsimport {NextUIProvider} from '@nextui-org/react'function MyApp({ Component, pageProps }) {  return (    <NextUIProvider>      <Component {...pageProps} />    </NextUIProvider>  )}export default MyApp;
```

### [Use NextUI Components](https://nextui.org/docs/guide/upgrade-to-v2#use-nextui-components-1)

Now you can import any NextUI component wherever you want:

```
import {Button} from '@nextui-org/react'export default function Page() {  return (    <div>      <Button>Click me</Button>    </div>  )}
```

### [Setup pnpm (optional)](https://nextui.org/docs/guide/upgrade-to-v2#setup-pnpm-optional-1)

If you are using pnpm, you need to add the following code to your `.npmrc` file:

```
public-hoist-pattern[]=*@nextui-org/theme*
```

After modfiying the `.npmrc` file, you need to run `pnpm install` again to ensure that the dependencies are installed correctly.

## [React upgrade steps](https://nextui.org/docs/guide/upgrade-to-v2#react-upgrade-steps)

### [Upgrade React version](https://nextui.org/docs/guide/upgrade-to-v2#upgrade-react-version)

NextUI v2 requires React 18 or later. To upgrade React, run the following command:

```
npm i react@latest react-dom@latest
```

### [Install Framer motion](https://nextui.org/docs/guide/upgrade-to-v2#install-framer-motion)

In v2, NextUI now requires `framer-motion` as a dependency. To install both, use the following command:

### [TailwindCSS Setup](https://nextui.org/docs/guide/upgrade-to-v2#tailwindcss-setup)

NextUI v2 now uses Tailwind CSS. Add the NextUI plugin to your `tailwind.config.js` file:

```
// tailwind.config.jsconst { nextui } = require("@nextui-org/react");/** @type {import('tailwindcss').Config} */module.exports = {  content: [    // ...    './node_modules/@nextui-org/theme/dist/**/*.{js,ts,jsx,tsx}'  ],  theme: {    extend: {},  },  darkMode: "class",  plugins: [nextui()]}
```

### [Provider Setup](https://nextui.org/docs/guide/upgrade-to-v2#provider-setup)

Go to `root` file and wrap the Component with the `NextUIProvider`:

```
// src/main.jsximport React from 'react'import ReactDOM from 'react-dom/client'import {NextUIProvider} from '@nextui-org/react'import App from './App'import './index.css'ReactDOM.createRoot(document.getElementById('root') as HTMLElement).render(  <React.StrictMode>    <NextUIProvider>      <App />    </NextUIProvider>  </React.StrictMode>,)
```

### [Use NextUI Components](https://nextui.org/docs/guide/upgrade-to-v2#use-nextui-components-2)

Now you can import any NextUI component wherever you want:

```
import {Button} from '@nextui-org/react'export default function Page() {  return (    <div>      <Button>Click me</Button>    </div>  )}
```

### [Setup pnpm (optional)](https://nextui.org/docs/guide/upgrade-to-v2#setup-pnpm-optional-2)

If you are using pnpm, you need to add the following code to your `.npmrc` file:

```
public-hoist-pattern[]=*@nextui-org/theme*
```

After modfiying the `.npmrc` file, you need to run `pnpm install` again to ensure that the dependencies are installed correctly.

> Please visit the [Release Notes](https://github.com/nextui-org/nextui/releases/tag/v2.0.0) for more information about the new features and breaking changes.