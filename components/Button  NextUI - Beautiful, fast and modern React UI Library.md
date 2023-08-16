Buttons allow users to perform actions and choose with a single tap.

[Storybook](https://storybook.nextui.org/?path=/story/components-button)[@nextui-org/button](https://www.npmjs.com/package/@nextui-org/button)[React Aria](https://react-spectrum.adobe.com/react-aria/useButton.html)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/button)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/button.ts)

___

[![Sponsored: Codeium](https://media.ethicalads.io/media/images/2023/05/Screen_Shot_2023-05-25_at_5.23.35_PM.png)](https://server.ethicalads.io/proxy/click/5146/02e8f7c2-075a-43b6-b28f-7838bbf80c92/)

## [Import](https://nextui.org/docs/components/button#import)

NextUI exports 2 button-related components:

-   **Button**: The main component to display a button.
-   **ButtonGroup**: A wrapper component to display a group of buttons.

```
import {Button, ButtonGroup} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/button#usage)

### [Disabled](https://nextui.org/docs/components/button#disabled)

### [Sizes](https://nextui.org/docs/components/button#sizes)

### [Radius](https://nextui.org/docs/components/button#radius)

### [Colors](https://nextui.org/docs/components/button#colors)

### [Variants](https://nextui.org/docs/components/button#variants)

### [Loading](https://nextui.org/docs/components/button#loading)

Pass the `isLoading` prop to display a [Spinner](https://nextui.org/docs/components/spinner) component inside the button.

You can also customize the loading spinner by passing the a custom component to the `spinner` prop.

### [With Icons](https://nextui.org/docs/components/button#with-icons)

You can add icons to the `Button` by passing the `startContent` or `endContent` props.

### [Icon Only](https://nextui.org/docs/components/button#icon-only)

You can also display a button without text by passing the `isIconOnly` prop and the desired icon as `children`.

### [Custom Styles](https://nextui.org/docs/components/button#custom-styles)

You can customize the `Button` component by passing custom Tailwind CSS classes to the component slots.

> Custom class names will override the default ones thanks to [Tailwind Merge](https://github.com/dcastil/tailwind-merge) library. It means that you don't need to worry about class conflicts.

### [Custom Implementation](https://nextui.org/docs/components/button#custom-implementation)

You can also use the `useButton` hook to create your own button component.

## [Button Group](https://nextui.org/docs/components/button#button-group)

### [Group Disabled](https://nextui.org/docs/components/button#group-disabled)

The `ButtonGroup` component also accepts the `isDisabled` prop to disable all buttons inside it.

### [Group Use case](https://nextui.org/docs/components/button#group-use-case)

A common use case for the `ButtonGroup` component is to display a group of two buttons one for the selected value and another for the `dropdown`.

> See the [Dropdown](https://nextui.org/docs/components/dropdown) component for more details.

## [Data Attributes](https://nextui.org/docs/components/button#data-attributes)

`Button` has the following attributes on the `root` element:

-   **data-hover**: When the button is being hovered. Based on [useHover](https://react-spectrum.adobe.com/react-aria/useHover.html)
-   **data-focus**: When the button is being focused. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-focus-visible**: When the button is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-disabled**: When the button is disabled. Based on `isDisabled` prop.
-   **data-pressed**: When the button is pressed. Based on [usePress](https://react-spectrum.adobe.com/react-aria/usePress.html)
-   **data-loading**: When the button is loading. Based on `isLoading` prop.

## [Accessibility](https://nextui.org/docs/components/button#accessibility)

-   Button has role of `button`.
-   Keyboard event support for Space and Enter keys.
-   Mouse and touch event handling, and press state management.
-   Keyboard focus management and cross browser normalization.

We recommend to read this [blog post](https://react-spectrum.adobe.com/blog/building-a-button-part-1.html) about the complexities of building buttons that work well across devices and interaction methods.

## [API](https://nextui.org/docs/components/button#api)

### [Button Props](https://nextui.org/docs/components/button#button-props)

### [Button Events](https://nextui.org/docs/components/button#button-events)

### [Button Group Props](https://nextui.org/docs/components/button#button-group-props)