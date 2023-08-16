Requirements:

___

[![Sponsored: Browserless](https://media.ethicalads.io/media/images/2023/02/Browserless_Ad_Feb_2023.png)](https://server.ethicalads.io/proxy/click/5152/d4ca527a-556d-4b4e-8e5a-6de72f3cf195/)

To use NextUI in your project, you need to follow the following steps:

## [Global Installation](https://nextui.org/docs/guide/installation#global-installation)

The easiest way to get started with NextUI is to use the global installation. Which means that all the components are imported from a single package.

Follow the steps below to install all NextUI components:

### [Install Packages](https://nextui.org/docs/guide/installation#install-packages)

To install NextUI, run one of the following commands in your terminal:

```
npm i @nextui-org/react framer-motion
```

### [Tailwind CSS Setup](https://nextui.org/docs/guide/installation#tailwind-css-setup)

NextUI is built on top of Tailwind CSS, so you need to install Tailwind CSS first. You can follow the official [installation guide](https://tailwindcss.com/docs/installation) to install Tailwind CSS. Then you need to add the following code to your `tailwind.config.js` file:

```
// tailwind.config.jsconst {nextui} = require("@nextui-org/react");/** @type {import('tailwindcss').Config} */module.exports = {  content: [    // ...    "./node_modules/@nextui-org/theme/dist/**/*.{js,ts,jsx,tsx}",  ],  theme: {    extend: {},  },  darkMode: "class",  plugins: [nextui()],};
```

### [Provider Setup](https://nextui.org/docs/guide/installation#provider-setup)

It is essential to add the `NextUIProvider` at the `root` of your application.

```
import * as React from "react";// 1. import `NextUIProvider` componentimport {NextUIProvider} from "@nextui-org/react";function App() {  // 2. Wrap NextUIProvider at the root of your app  return (    <NextUIProvider>      <YourApplication />    </NextUIProvider>  );}
```

### [Setup pnpm (optional)](https://nextui.org/docs/guide/installation#setup-pnpm-optional)

If you are using pnpm, you need to add the following code to your `.npmrc` file:

```
public-hoist-pattern[]=*@nextui-org/theme*
```

After modfiying the `.npmrc` file, you need to run `pnpm install` again to ensure that the dependencies are installed correctly.

## [Individual Installation](https://nextui.org/docs/guide/installation#individual-installation)

NextUI is also available as individual packages. You can install each package separately. This is useful if you want to reduce the size of your CSS bundle as it will only include styles for the components you're actually using.

> **Note**: JavaScript bundle size will not change due to tree shaking support in NextUI.

Follow the steps below to install each package separately:

### [Install Core Packages](https://nextui.org/docs/guide/installation#install-core-packages)

Although you can install each package separately, you need to install the core packages first to ensure that all components work correctly.

Run one of the following commands in your terminal to install the core packages:

```
npm i @nextui-org/theme @nextui-org/system framer-motion
```

### [Install Component](https://nextui.org/docs/guide/installation#install-component)

Now, let's install the component you want to use. For example, if you want to use the [Button](https://nextui.org/docs/components/button) component, you need to run one of the following commands in your terminal:

### [Tailwind CSS Setup](https://nextui.org/docs/guide/installation#tailwind-css-setup-1)

TailwindCSS setup changes a bit when you use individual packages. You only need to add the styles of the components your using to your `tailwind.config.js` file. For example, for the [Button](https://nextui.org/docs/components/button) component, you need to add the following code to your `tailwind.config.js` file:

```
// tailwind.config.jsconst {nextui} = require("@nextui-org/theme");/** @type {import('tailwindcss').Config} */module.exports = {  content: [    // single component styles    "./node_modules/@nextui-org/theme/dist/components/button.js",     // or you can use a glob pattern (multiple component styles)    './node_modules/@nextui-org/theme/dist/components/(button|snippet|code|input).js'  ],  theme: {    extend: {},  },  darkMode: "class",  plugins: [nextui()],};
```

### [Provider Setup](https://nextui.org/docs/guide/installation#provider-setup-1)

It is essential to add the `NextUIProvider` at the `root` of your application.

```
import * as React from "react";// 1. import `NextUIProvider` componentimport {NextUIProvider} from "@nextui-org/system";function App() {  // 2. Wrap NextUIProvider at the root of your app  return (    <NextUIProvider>      <YourApplication />    </NextUIProvider>  );}
```

### [Use the Component](https://nextui.org/docs/guide/installation#use-the-component)

Now, you can use the component you installed in your application:

```
import * as React from "react";import {Button} from "@nextui-org/button";function App() {  return (    <Button>Press me</Button>  );}
```

### [Setup pnpm (optional)](https://nextui.org/docs/guide/installation#setup-pnpm-optional-1)

If you are using pnpm, you need to add the following code to your `.npmrc` file:

```
public-hoist-pattern[]=*@nextui-org/theme*
```

After modfiying the `.npmrc` file, you need to run `pnpm install` again to ensure that the dependencies are installed correctly.

> Version 2 is only compatible with React 18 or later. If you are using React 17 or earlier, please use [version 1 of NextUI](https://v1.nextui.org/docs/getting-started).

## [Framework Guides](https://nextui.org/docs/guide/installation#framework-guides)

NextUI UI is compatible with your preferred framework. We have compiled comprehensive, step-by-step tutorials for the following frameworks: