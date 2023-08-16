Welcome to the NextUI documentation!

![NextUI banner](https://nextui.org/_next/image?url=%2Fnextui-banner.png&w=1920&q=100)

## [What is NextUI?](https://nextui.org/docs/guide/introduction#what-is-nextui)

NextUI is a UI library for React that helps you build beautiful and accessible user interfaces. Created on top of [Tailwind CSS](https://tailwindcss.com/) and [React Aria](https://react-spectrum.adobe.com/react-aria/index.html).

NextUI's primary goal is to streamline the development process, offering a beautiful and adaptable system design for an enhanced user experience.

___

## [FAQ](https://nextui.org/docs/guide/introduction#faq)

No, NextUI is an independent community project and is not related to Vercel.

### [How is NextUI different from TailwindCSS?](https://nextui.org/docs/guide/introduction#how-is-nextui-different-from-tailwindcss)

-   **TailwindCSS**:
    
    Tailwind CSS is a CSS Framework that provides atomic CSS classes to help you style components, leaving you to handle lots of other things like accessibility, component composition, keyboard navigation, style overrides, etc.
    
-   **NextUI**:
    
    NextUI is a UI library for React that combines the power of TailwindCSS with React Aria to provide a complete components (logic and styles) for building accessible and customizable user interfaces. Since NextUI uses TailwindCSS as its style engine, you can use all TailwindCSS classes within your NextUI components, ensuring optimal compiled CSS size.
    

### [How is NextUI different from TailwindCSS components libraries?](https://nextui.org/docs/guide/introduction#how-is-nextui-different-from-tailwindcss-components-libraries)

TailwindCSS components libraries such as [TailwindUI](https://tailwindui.com/) , [Flowbite](https://flowbite.com/), or [Preline](https://preline.co/), just to name a few, only offer a curated selection of TailwindCSS classes to style your components. They don't provide any React specific components, logic, props, composition, or accessibility features.  

In contrast to these libraries, NextUI is a complete UI library that provides a set of accessible and customizable components, hooks, and utilities.

### [How NextUI deals with TailwindCSS classes conflicts?](https://nextui.org/docs/guide/introduction#how-nextui-deals-with-tailwindcss-classes-conflicts)

We created a TailwindCSS utility library called [tailwind-variants](https://www.tailwind-variants.org/) that automatically handle TailwindCSS class conflicts. This ensures your custom classes will consistently override the default ones, eliminating any duplication.

### [Does NextUI use runtime CSS?](https://nextui.org/docs/guide/introduction#does-nextui-use-runtime-css)

No, As NextUI uses TailwindCSS as its style engine, it generates CSS at build time, eliminating the need for runtime CSS. This means that NextUI is fully compatible with the latest React and Next.js versions.

### [Does NextUI support TypeScript?](https://nextui.org/docs/guide/introduction#does-nextui-support-typescript)

Yes, NextUI is written in TypeScript and has full support for it.

### [Can I use NextUI with other front-end frameworks or libraries, such as Vue or Angular?](https://nextui.org/docs/guide/introduction#can-i-use-nextui-with-other-front-end-frameworks-or-libraries-such-as-vue-or-angular)

No, NextUI is specifically designed for React as it is built on top of React Aria. However, you can still use the NextUI components styling part with other frameworks or libraries.

### [Why NextUI uses Framer Motion?](https://nextui.org/docs/guide/introduction#why-nextui-uses-framer-motion)

We use [Framer Motion](https://www.framer.com/motion) to animate some components due to the complexity of the animations and their physics-based nature. Framer Motion allows us to handle these animations in a more straightforward and performant way in addition it is well tested and production ready.

___

We're excited to see the community adopt NextUI, raise issues, and provide feedback. Whether it's a feature request, bug report, or a project to showcase, please get involved!

## [Contributing](https://nextui.org/docs/guide/introduction#contributing)

PR's on NextUI are always welcome, please see our [contribution guidelines](https://github.com/nextui-org/nextui/blob/main/CONTRIBUTING.MD) to learn how you can contribute to this project.