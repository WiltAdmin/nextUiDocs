NextUI's plugin enables you to personalize the semantic colors of the theme such as `primary`, `secondary`, `success`, etc.

```
module.exports = {  plugins: [    nextui({      themes: {        light: {          // ...          colors: {},        },        dark: {          // ...          colors: {},        },        // ... custom themes      },    }),  ],};
```

[![Sponsored: MongoDB](https://media.ethicalads.io/media/images/2022/08/EthicalAds_240x180_3.jpg)](https://server.ethicalads.io/proxy/click/5097/86119dbd-5a79-47c6-820f-0218b6f82455/)

> **Note**: Colors configurations apply globally across all components.

## [Default Colors](https://nextui.org/docs/customization/colors#default-colors)

NextUI offers a default color palette right out of the box, perfect for when you're still undecided about your specific branding colors.

These colors are split into [Common Colors](https://nextui.org/docs/customization/colors#common-colors) and [Semantic Colors](https://nextui.org/docs/customization/colors#semantic-colors).

-   [Common Colors](https://nextui.org/docs/customization/colors#common-colors): Consistent across themes.
-   [Semantic Colors](https://nextui.org/docs/customization/colors#semantic-colors): Adjust according to the chosen theme.

### [Common Colors](https://nextui.org/docs/customization/colors#common-colors)

Common colors, like [TailwindCSS](https://tailwindcss.com/docs/customizing-colors) colors, remain consistent regardless of the theme.

To prevent conflicts with TailwindCSS colors, common colors are initially disabled but can be activated with the `addCommonColors` option.

```
module.exports = {  plugins: [    nextui({      addCommonColors: true,    }),  ],};
```

Enabling this option supplements some TailwindCSS default colors with the following:

```
module.exports = {  theme: {    extend: {      colors: {        white: "#FFFFFF",        black: "#000000",        blue: {          50: "#e6f1fe",          100: "#cce3fd",          200: "#99c7fb",          300: "#66aaf9",          400: "#338ef7",          500: "#006FEE",          600: "#005bc4",          700: "#004493",          800: "#002e62",          900: "#001731",        },        // .. rest of the colors      },    },  },};
```

## White & Black

## Blue

## Purple

## Green

## Red

## Pink

## Yellow

## Cyan

## Zinc

### [Semantic Colors](https://nextui.org/docs/customization/colors#semantic-colors)

Semantic colors adapt with the theme, delivering meaning and reinforcing your brand identity.

For an effective palette, we recommend using color ranges from `50` to `900`. You can use tools like [Eva Design System](https://colors.eva.design/), [Smart Watch](https://smart-swatch.netlify.app/), [Palette](https://palettte.app/) or [Color Box](https://colorbox.io/) to generate your palette.

> Semantic colors should be placed inside the `nextui` plugin options, not inside the TailwindCSS theme object.

```
module.exports = {  plugins: [    nextui({      themes: {        light: {          colors: {            background: "#FFFFFF", // or DEFAULT            foreground: "#11181C", // or 50 to 900 DEFAULT            primary: {              //... 50 to 900              foreground: "#FFFFFF",              DEFAULT: "#006FEE",            },            // ... rest of the colors          },        },        dark: {          colors: {            background: "#000000", // or DEFAULT            foreground: "#ECEDEE", // or 50 to 900 DEFAULT            primary: {              //... 50 to 900              foreground: "#FFFFFF",              DEFAULT: "#006FEE",            },          },          // ... rest of the colors        },        mytheme: {          // custom theme          extend: "dark",          colors: {            primary: {              DEFAULT: "#BEF264",              foreground: "#000000",            },            focus: "#BEF264",          },        },      },    }),  ],};
```

> Change the docs theme to see the semantic colors in action.

## Layout

## Content

## Base

## Default

## Primary

## Secondary

## Success

## Warning

## Danger

### [Using Semantic Colors](https://nextui.org/docs/customization/colors#using-semantic-colors)

Semantic colors can be applied anywhere in your project where colors are used, such as text color, border color, background color utilities, and more.

```
<div class="bg-primary-500 text-primary-50 rounded-small px-unit-2 py-unit-1">  This is a primary color box</div>
```

> **Note**: To know more about units see the [Layout Units](https://nextui.org/docs/customization/layout#using-units) section.

### [Javascript Variables](https://nextui.org/docs/customization/colors#javascript-variables)

Import semantic and common colors into your JavaScript files as follows:

```
import {commonColors, semanticColors} from "@nextui-org/theme";console.log(commonColors.white); // #FFFFFFconsole.log(commonColors.blue[500]); // #006FEEconsole.log(semanticColors.dark.warning.DEFAULT); // #FFC107console.log(semanticColors.light.primary.DEFAULT); // #006FEE
```

### [CSS Variables](https://nextui.org/docs/customization/colors#css-variables)

NextUI creates CSS variables using the format `--prefix-colorname-shade` for each semantic color. By default the prefix is `nextui`, but you can change it with the `prefix` option.

```
module.exports = {  plugins: [    nextui({      prefix: "myapp",    }),  ],};
```

Then you can use the CSS variables in your CSS files.

```
/* With default prefix */.my-component {  background-color: var(--nextui-primary-500);}/*  With custom prefix */.my-component {  background-color: var(--myapp-primary-500);}
```