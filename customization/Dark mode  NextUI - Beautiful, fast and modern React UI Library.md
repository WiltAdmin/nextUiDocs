As we mentioned before in the [Theme](https://nextui.org/docs/customization/theme) section NextUI comes with two default themes `light`and `dark`. So using the `dark` theme is as simple as adding it to the `className` of the `html` / `body` or `main` element.

```
// main.tsx or main.jsximport React from "react";import ReactDOM from "react-dom/client";import {NextUIProvider} from "@nextui-org/react";import App from "./App";import "./index.css";ReactDOM.createRoot(document.getElementById("root")).render(  <React.StrictMode>    <NextUIProvider>      <main className="dark text-foreground bg-background">        <App />      </main>    </NextUIProvider>  </React.StrictMode>,);
```

This will enable the dark mode for the whole application. However, many applications require the capability to switch between different themes. For this purpose, we recommend using a theme switch library or creating your own implementation.

[![Sponsored: MongoDB](https://media.ethicalads.io/media/images/2022/08/EthicalAds_240x180_3.jpg)](https://server.ethicalads.io/proxy/click/5097/86119dbd-5a79-47c6-820f-0218b6f82455/)

## [Using next-themes](https://nextui.org/docs/customization/dark-mode#using-next-themes)

For applications using [Next.js](https://nextui.org/docs/frameworks/nextjs), the [next-themes](https://github.com/pacocoursey/next-themes) library is an excellent choice. It comes packed with features that enhance the user experience when transitioning between themes.

> For more information, refer to the [next-themes](https://github.com/pacocoursey/next-themes) documentation.

### [Next.js App Directory Setup](https://nextui.org/docs/customization/dark-mode#nextjs-app-directory-setup)

### [Install next-themes](https://nextui.org/docs/customization/dark-mode#install-next-themes)

Install `next-themes` in your project.

### [Add next-themes provider](https://nextui.org/docs/customization/dark-mode#add-next-themes-provider)

Wrap your app with the `ThemeProvider` component from `next-themes`.

Go to your `app/providers.tsx` or `app/providers.jsx` (create it if it doesn't exist) and wrap the Component with the `NextUIProvider` and the `next-themes` provider components.

```
// app/providers.tsx'use client'import {NextUIProvider} from '@nextui-org/react'import {ThemeProvider as NextThemesProvider} from "next-themes";export function Providers({children}: { children: React.ReactNode }) {  return (    <NextUIProvider>      <NextThemesProvider attribute="class" defaultTheme="dark">        {children}      </NextThemesProvider>    </NextUIProvider>  )}
```

> Note: We're using the `class` attribute to switch between themes, this is because NextUI uses the `className` attribute.

### [Add the theme switcher](https://nextui.org/docs/customization/dark-mode#add-the-theme-switcher)

Add the theme switcher to your app.

```
// app/components/ThemeSwitcher.tsximport {useTheme} from "next-themes";export const ThemeSwitcher = () => {  const { theme, setTheme } = useTheme()  return (    <div>      The current theme is: {theme}      <button onClick={() => setTheme('light')}>Light Mode</button>      <button onClick={() => setTheme('dark')}>Dark Mode</button>    </div>  )};
```

> **Note**: You can use any theme name you want, but make sure it exits in your `tailwind.config.js` file. See [Create Theme](https://nextui.org/docs/customization/create-theme) for more details.

### [Next.js Pages Directory Setup](https://nextui.org/docs/customization/dark-mode#nextjs-pages-directory-setup)

### [Install next-themes](https://nextui.org/docs/customization/dark-mode#install-next-themes-1)

Install `next-themes` in your project.

### [Add next-themes provider](https://nextui.org/docs/customization/dark-mode#add-next-themes-provider-1)

Go to pages`/_app.js` or `pages/_app.tsx` (create it if it doesn't exist) and wrap the Component with the `NextUIProvider` and the `next-themes` provider components.

```
// pages/_app.jsimport {NextUIProvider} from '@nextui-org/react'import {ThemeProvider as NextThemesProvider} from "next-themes";function MyApp({ Component, pageProps }) {  return (    <NextUIProvider>      <NextThemesProvider attribute="class" defaultTheme="dark">        <Component {...pageProps} />      </NextThemesProvider>    </NextUIProvider>  )}export default MyApp;
```

> Note: We're using the `class` attribute to switch between themes, this is because NextUI uses the `className` attribute.

### [Add the theme switcher](https://nextui.org/docs/customization/dark-mode#add-the-theme-switcher-1)

Add the theme switcher to your app.

```
// components/ThemeSwitcher.tsximport {useTheme} from "next-themes";export const ThemeSwitcher = () => {  const { theme, setTheme } = useTheme()  return (    <div>      The current theme is: {theme}      <button onClick={() => setTheme('light')}>Light Mode</button>      <button onClick={() => setTheme('dark')}>Dark Mode</button>    </div>  )};
```

> **Note**: You can use any theme name you want, but make sure it exits in your `tailwind.config.js` file. See [Create Theme](https://nextui.org/docs/customization/create-theme) for more details.

## [Using use-dark-mode hook](https://nextui.org/docs/customization/dark-mode#using-use-dark-mode-hook)

In case you're using plain React with [Vite](https://nextui.org/docs/frameworks/vite) or [Create React App](https://create-react-app.dev/) you can use the [use-dark-mode](https://github.com/donavon/use-dark-mode) hook to switch between themes.

> See the [use-dark-mode](https://github.com/donavon/use-dark-mode) documentation for more details.

### [Install use-dark-mode](https://nextui.org/docs/customization/dark-mode#install-use-dark-mode)

Install `use-dark-mode` in your project.

```
npm install use-dark-mode
```

### [Add the current theme to the main element](https://nextui.org/docs/customization/dark-mode#add-the-current-theme-to-the-main-element)

```
// App.tsx or App.jsximport React from "react";import useDarkMode from "use-dark-mode";export default function App() {  const darkMode = useDarkMode(false);  return (    <main className={`${darkMode.value ? 'dark' : ''} text-foreground bg-background`}>      <App />    </main>  )}
```

### [Add the theme switcher](https://nextui.org/docs/customization/dark-mode#add-the-theme-switcher-2)

Add the theme switcher to your app.

```
// components/ThemeSwitcher.tsximport useDarkMode from "use-dark-mode";export const ThemeSwitcher = () => {  const darkMode = useDarkMode(false);  return (    <div>      <button onClick={darkMode.disable}>Light Mode</button>      <button onClick={darkMode.enable}>Dark Mode</button>    </div>  )};
```

> **Note**: You can use any theme name you want, but make sure it exits in your `tailwind.config.js` file. See [Create Theme](https://nextui.org/docs/customization/create-theme) for more details.