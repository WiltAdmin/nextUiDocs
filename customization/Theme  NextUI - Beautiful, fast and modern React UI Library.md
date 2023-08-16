Theming is a key element in designing user interfaces (UIs). It enables the application of a consistent aesthetic across your application, enhancing the user experience and maintaining visual uniformity.

In NextUI, we facilitate easy and flexible theme customization using a TailwindCSS plugin. This plugin, which is based on the [tw-colors](https://github.com/L-Blondy/tw-colors) plugin developed by [L-Blondy](https://github.com/L-Blondy), allows you to customize color schemes, layout configurations, and more, across different components of your application.

## [What is a Theme?](https://nextui.org/docs/customization/theme#what-is-a-theme)

A theme, in the context of NextUI, is a predefined set of colors, layout attributes, and other UI elements that you can consistently apply across your application. Themes ensure visual consistency, enrich the user experience, and simplify the management and updates of your app's look and feel.

## [Setup](https://nextui.org/docs/customization/theme#setup)

The first step to using NextUI's theming capability is adding the `nextui` plugin to your `tailwind.config.js` file. Below is an example of how to do this:

```
// tailwind.config.jsconst {nextui} = require("@nextui-org/react");/** @type {import('tailwindcss').Config} */module.exports = {  content: [    // ...    "./node_modules/@nextui-org/theme/dist/**/*.{js,ts,jsx,tsx}",  ],  theme: {    extend: {},  },  darkMode: "class",  plugins: [nextui()],};
```

### [Usage](https://nextui.org/docs/customization/theme#usage)

After adding the plugin to your `tailwind.config.js` file, you can utilize any of the default themes (light/dark) or a custom one. Here's how you can apply these themes in your `main.jsx` or `main.tsx`:

Go to the src directory and inside `main.jsx` or `main.tsx`, apply the following class names to the root element:

-   `light` for the light theme.
-   `dark` for the dark theme.
-   `text-foreground` to set the text color.
-   `bg-background` to set the background color.

```
// main.tsx or main.jsximport React from "react";import ReactDOM from "react-dom/client";import {NextUIProvider} from "@nextui-org/react";import App from "./App";import "./index.css";ReactDOM.createRoot(document.getElementById("root")).render(  <React.StrictMode>    <NextUIProvider>      <main className="dark text-foreground bg-background">        <App />      </main>    </NextUIProvider>  </React.StrictMode>,);
```

> **Note**: See the [Colors](https://nextui.org/docs/customization/colors) section to learn more about the color classes.

### [Default Plugin Options](https://nextui.org/docs/customization/theme#default-plugin-options)

The `nextui` plugin provides a default structure. It is outlined as follows:

```
module.exports = {  plugins: [    nextui({      prefix: "nextui", // prefix for themes variables      addCommonColors: false, // override common colors (e.g. "blue", "green", "pink").      defaultTheme: "light", // default theme from the themes object      defaultExtendTheme: "light", // default theme to extend on custom themes      layout: {}, // common layout tokens (applied to all themes)      themes: {        light: {          layout: {}, // light theme layout tokens          colors: {}, // light theme colors        },        dark: {          layout: {}, // dark theme layout tokens          colors: {}, // dark theme colors        },        // ... custom themes      },    }),  ],};
```

### [Themes Options](https://nextui.org/docs/customization/theme#themes-options)

These are the options that you can use to apply custom configurations to your themes.

```
module.exports = {  plugins: [    nextui({      themes: {        light: {          layout: {},          colors: {}        },        dark: {          layout: {},          colors: {}        },        ... // custom themes      }    })  ]}
```

### [Nested themes](https://nextui.org/docs/customization/theme#nested-themes)

NextUI supports nested themes, allowing you to apply different themes to different sections of your application:

```
<html class="dark">  ...  <div class="light">...</div>  <div class="purple-dark">...</div></html>
```

### [Theme based variants](https://nextui.org/docs/customization/theme#theme-based-variants)

NextUI enables you to apply TailwindCSS styles based on the currently active theme. Below are examples of how to do this:

```
<!-- In dark theme, background will be dark and text will be light.   In light theme, background will be light and text will be dark --><div class="dark dark:bg-gray-800 dark:text-white bg-white text-black">  ...  <div>Text color changes based on theme</div></div><div class="light light:bg-gray-100 light:text-black bg-black text-white">  ...  <div>Text color changes based on theme</div></div>
```

### [API Reference](https://nextui.org/docs/customization/theme#api-reference)

The following table provides an overview of the various attributes you can use when working with themes in NextUI:

### [Types](https://nextui.org/docs/customization/theme#types)

#### [ConfigThemes](https://nextui.org/docs/customization/theme#configthemes)

```
type ConfigTheme = {  extend?: "light" | "dark"; // base theme to extend  layout?: LayoutTheme; // see LayoutTheme  colors?: ThemeColors; // see ThemeColors};type ConfigThemes = Record<string, ConfigTheme>;
```

#### [LayoutTheme](https://nextui.org/docs/customization/theme#layouttheme)

```
type BaseThemeUnit = {  small?: string;  medium?: string;  large?: string;};type FontThemeUnit = {  small?: string;  medium?: string;  large?: string;  tiny?: string;};interface LayoutTheme {  /**   * Base unit token that defines a consistent spacing scale across   * the components.   */  spacingUnit?: number;  /**   * The default font size applied across the components.   */  fontSize?: FontThemeUnit;  /**   * The default line height applied across the components.   */  lineHeight?: FontThemeUnit;  /**   * The default radius applied across the components.   * we recommend to use `rem` units.   */  radius?: BaseThemeUnit;  /**   * A number between 0 and 1 that is applied as opacity-[value] when   * the component is disabled.   */  disabledOpacity?: string | number;  /**   * The default height applied to the divider component.   * we recommend to use `px` units.   */  dividerWeight?: string;  /**   * The border width applied across the components.   */  borderWidth?: BaseThemeUnit;  /**   * The box shadow applied across the components.   */  boxShadow?: BaseThemeUnit;}
```

#### [ThemeColors](https://nextui.org/docs/customization/theme#themecolors)

```
type ColorScale = {  50: string;  100: string;  200: string;  300: string;  400: string;  500: string;  600: string;  700: string;  800: string;  900: string;  foreground: string; // contrast color  DEFAULT: string;};type BaseColors = {  background: ColorScale; // the page background color  foreground: ColorScale; // the page text color  divider: ColorScale; // used for divider and single line border  overlay: ColorScale; // used for modal, popover, etc.  focus: ColorScale; // used for focus state outline  content1: ColorScale; // used for card, modal, popover, etc.  content2: ColorScale;  content3: ColorScale;  content4: ColorScale;};// brand colorstype ThemeColors = BaseColors & {  default: ColorScale;  primary: ColorScale;  secondary: ColorScale;  success: ColorScale;  warning: ColorScale;  danger: ColorScale;};
```