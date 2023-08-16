Links allow users to click their way from page to page. This component is styled to resemble a hyperlink and semantically renders an `<a>`

[Storybook](https://storybook.nextui.org/?path=/story/components-link)[@nextui-org/link](https://www.npmjs.com/package/@nextui-org/link)[React Aria](https://react-spectrum.adobe.com/react-aria/useLink.html)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/link)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/link.ts)

___

[![Sponsored: Browserless](https://media.ethicalads.io/media/images/2023/02/Browserless_Ad_Feb_2023.png)](https://server.ethicalads.io/proxy/click/5152/364b3784-ddb1-4fcf-9c8d-fa07a7f600ea/)

## [Import](https://nextui.org/docs/components/link#import)

```
import {Link} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/link#usage)

### [Disabled](https://nextui.org/docs/components/link#disabled)

### [Sizes](https://nextui.org/docs/components/link#sizes)

### [Colors](https://nextui.org/docs/components/link#colors)

### [Underline](https://nextui.org/docs/components/link#underline)

### [External](https://nextui.org/docs/components/link#external)

If you pass the `isExternal` prop, the link will have the `target="_blank"` and `rel="noopener noreferrer"` attributes.

### [Custom Anchor Icon](https://nextui.org/docs/components/link#custom-anchor-icon)

### [Block Link](https://nextui.org/docs/components/link#block-link)

If you pass the `isBlock` prop, the link will be rendered as a block element with a `hover` effect.

### [Polymorphic Component](https://nextui.org/docs/components/link#polymorphic-component)

NextUI components expose a `as` prop that allows you to customize the React element type that is used to render the component.

### [Usage with Next.js](https://nextui.org/docs/components/link#usage-with-nextjs)

### [Custom Implementation](https://nextui.org/docs/components/link#custom-implementation)

In case you need to customize the link even further, you can use the `useLink` hook to create your own implementation.

## [Data Attributes](https://nextui.org/docs/components/link#data-attributes)

`Link` has the following attributes on the `root` element:

-   **data-focus**: When the link is being focused. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html)
-   **data-focus-visible**: When the link is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html)
-   **data-disabled**: When the link is disabled. Based on `isDisabled` prop.

## [Accessibility](https://nextui.org/docs/components/link#accessibility)

-   Support for mouse, touch, and keyboard interactions.
-   Support for navigation links via `<a>` elements or custom element types via ARIA.
-   Support for disabled links.
-   Keyboard users may activate links using the Enter key.

## [API](https://nextui.org/docs/components/link#api)

### [Link Props](https://nextui.org/docs/components/link#link-props)

### [Link Events](https://nextui.org/docs/components/link#link-events)