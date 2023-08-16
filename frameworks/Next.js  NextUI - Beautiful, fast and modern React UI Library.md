Requirements:

___

To use NextUI in your Next.js project, you need to follow the steps below, depending on your project structure.

## [App directory Setup](https://nextui.org/docs/frameworks/nextjs#app-directory-setup)

Next.js 13 introduces a new `app/` directory structure. By default it uses Server Components. As NextUI components use React hooks, we added the `use client;` at build time, so you can import them directly in your React Server Components (RSC).

### [create-next-app](https://nextui.org/docs/frameworks/nextjs#create-next-app)

If you are starting a new project, you can run one of the following command to create a Next.js project pre-configured with NextUI:

```
npx create-next-app -e https://github.com/nextui-org/next-app-template
```

### [Manual Installation](https://nextui.org/docs/frameworks/nextjs#manual-installation)

### [Add dependencies](https://nextui.org/docs/frameworks/nextjs#add-dependencies)

In your Next.js project, run one of the following command to install NextUI:

```
npm i @nextui-org/react framer-motion
```

### [Tailwind CSS Setup](https://nextui.org/docs/frameworks/nextjs#tailwind-css-setup)

NextUI is built on top of Tailwind CSS, so you need to install Tailwind CSS first. You can follow the official [installation guide](https://tailwindcss.com/docs/guides/nextjs) to install Tailwind CSS. Then you need to add the following code to your `tailwind.config.js` file:

```
// tailwind.config.jsconst { nextui } = require("@nextui-org/react");/** @type {import('tailwindcss').Config} */module.exports = {  content: [    // ...    './node_modules/@nextui-org/theme/dist/**/*.{js,ts,jsx,tsx}'  ],  theme: {    extend: {},  },  darkMode: "class",  plugins: [nextui()]}
```

### [Setup Provider](https://nextui.org/docs/frameworks/nextjs#setup-provider)

Go to your `app/providers.tsx` or `app/providers.jsx` (create it if it doesn't exist) and wrap the Component with the `NextUIProvider`:

```
// app/providers.tsx'use client'import {NextUIProvider} from '@nextui-org/react'export function Providers({children}: { children: React.ReactNode }) {  return (    <NextUIProvider>      {children}    </NextUIProvider>  )}
```

### [Add Provider to Root](https://nextui.org/docs/frameworks/nextjs#add-provider-to-root)

Now, Go to your `root` layout page and wrap it with the `NextUIProvider`:

```
// app/layout.tsximport {Providers} from "./providers";export default function RootLayout({children}: { children: React.ReactNode }) {  return (    <html lang="en" className='dark'>      <body>        <Providers>          {children}        </Providers>      </body>    </html>  );}
```

> **Note**: NextUI automatically add two themes `light` and `dark` to your application. You can use any of them by adding the `dark`/`light` class to the `html` tag. See the [theme docs](https://nextui.org/docs/customization/customize-theme) for more details.

### [Use NextUI Components](https://nextui.org/docs/frameworks/nextjs#use-nextui-components)

Now you can import any NextUI component directly in your Server Components without needing to use the `use client;` directive:

```
// app/page.tsximport {Button} from '@nextui-org/button'; export default function Page() {  return (    <div>      <Button>Click me</Button>    </div>  )}
```

> **Important 🚨**: Note that you need to import the component from the individual package, not the from `@nextui-org/react`.

### [Setup pnpm (optional)](https://nextui.org/docs/frameworks/nextjs#setup-pnpm-optional)

If you are using pnpm, you need to add the following code to your `.npmrc` file:

```
public-hoist-pattern[]=*@nextui-org/theme*
```

After modfiying the `.npmrc` file, you need to run `pnpm install` again to ensure that the dependencies are installed correctly.

## [Pages Directory Setup](https://nextui.org/docs/frameworks/nextjs#pages-directory-setup)

If you are using the `/pages` Next.js project structure, you need to follow the steps below.

### [create-next-app](https://nextui.org/docs/frameworks/nextjs#create-next-app-1)

If you are starting a new project, you can run one of the following command to create a Next.js project pre-configured with NextUI:

```
npx create-next-app -e https://github.com/nextui-org/next-pages-template
```

### [Manual Installation](https://nextui.org/docs/frameworks/nextjs#manual-installation-1)

### [Add dependencies](https://nextui.org/docs/frameworks/nextjs#add-dependencies-1)

In your Next.js project, run one of the following command to install NextUI:

```
npm i @nextui-org/react framer-motion
```

### [Tailwind CSS Setup](https://nextui.org/docs/frameworks/nextjs#tailwind-css-setup-1)

NextUI is built on top of Tailwind CSS, so you need to install Tailwind CSS first. You can follow the official [installation guide](https://tailwindcss.com/docs/guides/nextjs) to install Tailwind CSS. Then you need to add the following code to your `tailwind.config.js` file:

```
// tailwind.config.jsconst { nextui } = require("@nextui-org/react");/** @type {import('tailwindcss').Config} */module.exports = {  content: [    // ...    './node_modules/@nextui-org/theme/dist/**/*.{js,ts,jsx,tsx}'  ],  theme: {    extend: {},  },  darkMode: "class",  plugins: [nextui()]}
```

### [Setup Provider](https://nextui.org/docs/frameworks/nextjs#setup-provider-1)

Go to pages`/_app.js` or `pages/_app.tsx` (create it if it doesn't exist) and wrap the Component with the `NextUIProvider`:

```
// pages/_app.jsimport {NextUIProvider} from '@nextui-org/react'function MyApp({ Component, pageProps }) {  return (    <NextUIProvider>      <Component {...pageProps} />    </NextUIProvider>  )}export default MyApp;
```

### [Use NextUI Components](https://nextui.org/docs/frameworks/nextjs#use-nextui-components-1)

Now you can import any NextUI component wherever you want:

```
import {Button} from '@nextui-org/react'export default function Page() {  return (    <div>      <Button>Click me</Button>    </div>  )}
```

### [Setup pnpm (optional)](https://nextui.org/docs/frameworks/nextjs#setup-pnpm-optional-1)

If you are using pnpm, you need to add the following code to your `.npmrc` file:

```
public-hoist-pattern[]=*@nextui-org/theme*
```

After modfiying the `.npmrc` file, you need to run `pnpm install` again to ensure that the dependencies are installed correctly.

> Version 2 is only compatible with React 18 or later. If you are using React 17 or earlier, please use [version 1 of NextUI](https://v1.nextui.org/docs/getting-started).