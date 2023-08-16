The Switch component is used as an alternative between checked and not checked states.

[Storybook](https://storybook.nextui.org/?path=/story/components-switch)[@nextui-org/switch](https://www.npmjs.com/package/@nextui-org/switch)[React Aria](https://react-spectrum.adobe.com/react-aria/useSwitch.html)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/switch)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/toggle.ts)

___

[![Sponsored: Browserless](https://media.ethicalads.io/media/images/2023/02/Browserless_Ad_Feb_2023_JZvbtJs.png)](https://server.ethicalads.io/proxy/click/5153/155a18f4-b2b1-494e-a3e5-ef8648d4ffc7/)

## [Import](https://nextui.org/docs/components/switch#import)

```
import {Switch} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/switch#usage)

### [With Label](https://nextui.org/docs/components/switch#with-label)

### [Disabled](https://nextui.org/docs/components/switch#disabled)

### [Sizes](https://nextui.org/docs/components/switch#sizes)

### [Colors](https://nextui.org/docs/components/switch#colors)

### [With Thumb Icon](https://nextui.org/docs/components/switch#with-thumb-icon)

### [With Icons](https://nextui.org/docs/components/switch#with-icons)

You can also add icons to start and end of the switch by using `startContent` and `endContent` props.

### [Controlled](https://nextui.org/docs/components/switch#controlled)

> **Note**: NextUI `Switch` also supports native events like `onChange`, useful for form libraries such as [Formik](https://formik.org/) and [React Hook Form](https://react-hook-form.com/).

## [Slots](https://nextui.org/docs/components/switch#slots)

-   **base**: Base slot for the switch. It is the main wrapper.
-   **wrapper**: The wrapper of the start icon, end icon and thumb.
-   **thumb**: The thumb element of the switch. It is the circle element.
-   **label**: The label slot of the switch.
-   **startContent**:The icon slot at the start of the switch.
-   **endContent**: The icon slot at the end of the switch.
-   **thumbIcon**: The icon slot inside the thumb.

### [Custom Styles](https://nextui.org/docs/components/switch#custom-styles)

You can customize the `Switch` component by passing custom Tailwind CSS classes to the component slots.

### [Custom Implementation](https://nextui.org/docs/components/switch#custom-implementation)

In case you need to customize the switch even further, you can use the `useSwitch` hook to create your own implementation.

## [Data Attributes](https://nextui.org/docs/components/switch#data-attributes)

`Switch` has the following attributes on the `root` element:

-   **data-selected**: When the switch is checked. Based on `isSelected` prop.
-   **data-pressed**: When the switch is pressed. Based on [usePress](https://react-spectrum.adobe.com/react-aria/usePress.html)
-   **data-readonly**: When the switch is readonly. Based on `isReadOnly` prop.
-   **data-hover**: When the switch is being hovered. Based on [useHover](https://react-spectrum.adobe.com/react-aria/useHover.html)
-   **data-focus**: When the switch is being focused. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-focus-visible**: When the switch is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-disabled**: When the switch is disabled. Based on `isDisabled` prop.

## [Accessibility](https://nextui.org/docs/components/switch#accessibility)

-   Built with a native HTML `<input>` element.
-   Full support for browser features like form autofill.
-   Keyboard focus management and cross browser normalization.
-   Keyboard event support for Tab and Space keys.
-   Labeling support for assistive technology.
-   Exposed as a switch to assistive technology via ARIA

## [API](https://nextui.org/docs/components/switch#api)

### [Switch Props](https://nextui.org/docs/components/switch#switch-props)

### [Switch Events](https://nextui.org/docs/components/switch#switch-events)

### [Types](https://nextui.org/docs/components/switch#types)

#### [Switch Icon Props](https://nextui.org/docs/components/switch#switch-icon-props)

```
type IconProps = {  "data-checked": string;  width: string;  height: string;  isSelected: boolean;  className: string;};type CheckboxIconProps = ReactNode | ((props: IconProps) => ReactNode);
```