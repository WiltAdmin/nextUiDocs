As outlined in preceding sections, NextUI presents two predefined themes, `light` and `dark`. These themes are inherently flexible, allowing you to tailor them to your specific preferences or project needs.

Furthermore, you have the option to create your own theme based on the default ones. Each theme incorporates [Layout](https://nextui.org/docs/customization/layout) tokens and [Color](https://nextui.org/docs/customization/colors) tokens, designed to facilitate your customization process.

[![Sponsored: MongoDB](https://media.ethicalads.io/media/images/2022/08/EthicalAds_240x180_3.jpg)](https://server.ethicalads.io/proxy/click/5097/86119dbd-5a79-47c6-820f-0218b6f82455/)

## [Customizing Layout](https://nextui.org/docs/customization/customize-theme#customizing-layout)

You can modify a variety of layout aspects, including spacing units, font sizes, line heights, radius, and more.

Layout tokens can be applied globally across all themes or specifically to a chosen theme.

### [Global Layout Customization](https://nextui.org/docs/customization/customize-theme#global-layout-customization)

Suppose you require a smaller border radius, a thinner border width, and more opaque disabled elements across all themes. You can implement these changes by adding the following code to your `tailwind.config.js` file.

```
// tailwind.config.jsconst {nextui} = require("@nextui-org/react");/** @type {import('tailwindcss').Config} */module.exports = {  plugins: [    nextui({      layout: {        disabledOpacity: "0.3", // opacity-[0.3]        radius: {          small: "2px", // rounded-small          medium: "4px", // rounded-medium          large: "6px", // rounded-large        },        borderWidth: {          small: "1px", // border-small          medium: "1px", // border-medium          large: "2px", // border-large        },      },      themes: {        light: {},        dark: {},      },    }),  ],};
```

As NextUI components employ layout tokens, the modifications will be reflected across all components that utilize them. For instance, the [Button](https://nextui.org/docs/components/button) component uses the `radius` token to set the border radius and the `borderWidth` token to define the border width when the variant is `bordered`.

So let's see how the [Button](https://nextui.org/docs/components/button) component looks like after the changes.

```
import {Button} from "@nextui-org/react";export default function App() {  return (    <div className="flex gap-4">      <Button variant="bordered" radius="md">        Button      </Button>      <Button isDisabled color="primary" radius="md">        Disabled      </Button>    </div>  );}
```

> See the [Layout](https://nextui.org/docs/customization/layout#default-layout) section for more details about the available tokens.

### [Customizing Colors](https://nextui.org/docs/customization/customize-theme#customizing-colors)

Now, Let's say you wish to modify the primary and focus colors of the dark theme. This can be achieved by adding the following code to your `tailwind.config.js` file.

```
// tailwind.config.jsconst {nextui} = require("@nextui-org/react");/** @type {import('tailwindcss').Config} */module.exports = {  plugins: [    nextui({      themes: {        dark: {          colors: {            primary: {              DEFAULT: "#BEF264",              foreground: "#000000",            },            focus: "#BEF264",          },        },      },    }),  ],};
```

This modification will impact all components using the `primary` color. For instance, the [Button](https://nextui.org/docs/components/button) component uses the `primary` color as background color when the variant is `solid` or `ghost`.

```
import {Button} from "@nextui-org/react";export default function App() {  return (    <div className="flex gap-4">      <Button color="primary" variant="solid">Solid</Button>      <Button color="primary" variant="ghost">Ghost</Button>    </div>  );}
```

> 🎉 That's it! You have successfully customized the default theme. See the [Colors](https://nextui.org/docs/customization/colors) section for more details about the available semantic colors and color tokens.