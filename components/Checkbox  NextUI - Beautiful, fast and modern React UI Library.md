Checkboxes allow users to select multiple items from a list of individual items, or to mark one individual item as selected.

[Storybook](https://storybook.nextui.org/?path=/story/components-checkbox)[@nextui-org/checkbox](https://www.npmjs.com/package/@nextui-org/checkbox)[React Aria](https://react-spectrum.adobe.com/react-aria/useCheckbox.html)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/checkbox)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/checkbox.ts)

___

[![Sponsored: Codeium](https://media.ethicalads.io/media/images/2023/05/Screen_Shot_2023-05-25_at_5.23.35_PM.png)](https://server.ethicalads.io/proxy/click/5146/02e8f7c2-075a-43b6-b28f-7838bbf80c92/)

## [Import](https://nextui.org/docs/components/checkbox#import)

```
import {Checkbox} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/checkbox#usage)

### [Disabled](https://nextui.org/docs/components/checkbox#disabled)

### [Sizes](https://nextui.org/docs/components/checkbox#sizes)

### [Colors](https://nextui.org/docs/components/checkbox#colors)

### [Radius](https://nextui.org/docs/components/checkbox#radius)

### [Indeterminate](https://nextui.org/docs/components/checkbox#indeterminate)

The `isIndeterminate` prop sets a `Checkbox` to an indeterminate state, overriding its appearance and maintaining it until set to `false`, regardless of user interaction.

### [Line Through](https://nextui.org/docs/components/checkbox#line-through)

### [Custom Check Icon](https://nextui.org/docs/components/checkbox#custom-check-icon)

### [Controlled](https://nextui.org/docs/components/checkbox#controlled)

> **Note**: NextUI `Checkbox` also supports native events like `onChange`, useful for form libraries such as [Formik](https://formik.org/) and [React Hook Form](https://react-hook-form.com/).

## [Slots](https://nextui.org/docs/components/checkbox#slots)

-   **base**: Checkbox wrapper, it handles alignment, placement, and general appearance.
-   **wrapper**: An inner container that includes styles for relative positioning, flex properties, overflow handling and managing hover and selected states.
-   **icon**: Icon within the checkbox, controlling size, visibility, and changes when checked.
-   **label**: The text associated with the checkbox.

### [Custom Styles](https://nextui.org/docs/components/checkbox#custom-styles)

You can customize the `Checkbox` component by passing custom Tailwind CSS classes to the component slots.

### [Custom Implementation](https://nextui.org/docs/components/checkbox#custom-implementation)

In case you need to customize the checkbox even further, you can use the `useCheckbox` hook to create your own implementation.

> **Note**: We used [Tailwind Variants](https://www.tailwind-variants.org/) to implement the styles above, you can use any other library such as [clsx](https://www.npmjs.com/package/clsx) to achieve the same result.

## [Data Attributes](https://nextui.org/docs/components/checkbox#data-attributes)

`Checkbox` has the following attributes on the `root` element:

-   **data-selected**: When the checkbox is checked. Based on `isSelected` prop.
-   **data-pressed**: When the checkbox is pressed. Based on [usePress](https://react-spectrum.adobe.com/react-aria/usePress.html)
-   **data-invalid**: When the checkbox is invalid. Based on `validationState` prop.
-   **data-readonly**: When the checkbox is readonly. Based on `isReadOnly` prop.
-   **data-indeterminate**: When the checkbox is indeterminate. Based on `isIndeterminate` prop.
-   **data-hover**: When the checkbox is being hovered. Based on [useHover](https://react-spectrum.adobe.com/react-aria/useHover.html)
-   **data-focus**: When the checkbox is being focused. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-focus-visible**: When the checkbox is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-disabled**: When the checkbox is disabled. Based on `isDisabled` prop.
-   **data-loading**: When the checkbox is loading. Based on `isLoading` prop.

## [Accessibility](https://nextui.org/docs/components/checkbox#accessibility)

-   Built with a native HTML `<input>` element.
-   Full support for browser features like form autofill.
-   Keyboard focus management and cross browser normalization.
-   Keyboard event support for Tab and Space keys.
-   Labeling support for assistive technology.
-   Indeterminate state support.

## [API](https://nextui.org/docs/components/checkbox#api)

### [Checkbox Props](https://nextui.org/docs/components/checkbox#checkbox-props)

### [Checkbox Events](https://nextui.org/docs/components/checkbox#checkbox-events)

### [Types](https://nextui.org/docs/components/checkbox#types)

#### [Checkbox Icon Props](https://nextui.org/docs/components/checkbox#checkbox-icon-props)

```
type IconProps = {  "data-checked": string;  isSelected: boolean;  isIndeterminate: boolean;  disableAnimation: boolean;  className: string;};type CheckboxIconProps = ReactNode | ((props: IconProps) => ReactNode);
```