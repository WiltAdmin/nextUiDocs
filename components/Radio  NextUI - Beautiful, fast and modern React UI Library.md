## Radio group

Radio Group allow users to select a single option from a list of mutually exclusive options.

[Storybook](https://storybook.nextui.org/?path=/story/components-radio)[@nextui-org/radio](https://www.npmjs.com/package/@nextui-org/radio)[React Aria](https://react-spectrum.adobe.com/react-aria/useRadioGroup.html)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/radio)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/radio.ts)

___

[![Sponsored: Aptible](https://media.ethicalads.io/media/images/2023/08/Logo_Ad_2.jpg)](https://server.ethicalads.io/proxy/click/5201/8fe8aed7-c1e0-4dd7-a5f6-aba193455ece/)

## [Import](https://nextui.org/docs/components/radio-group#import)

```
import {RadioGroup, Radio} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/radio-group#usage)

### [Disabled](https://nextui.org/docs/components/radio-group#disabled)

### [Default Value](https://nextui.org/docs/components/radio-group#default-value)

### [With Description](https://nextui.org/docs/components/radio-group#with-description)

### [Horizontal](https://nextui.org/docs/components/radio-group#horizontal)

### [Controlled](https://nextui.org/docs/components/radio-group#controlled)

You can use the `value` and `onValueChange` properties to control the radio input value.

> **Note**: NextUI `Radio` also supports native events like `onChange`, useful for form libraries such as [Formik](https://formik.org/) and [React Hook Form](https://react-hook-form.com/).

## [Slots](https://nextui.org/docs/components/radio-group#slots)

-   RadioGroup Slots
    
    -   **base**: Radio group root wrapper, it wraps the label and the wrapper.
    -   **wrapper**: Radio group wrapper, it wraps all Radios.
    -   **label**: Radio group label, it is placed before the wrapper.
    -   **description**: Description slot for the radio group.
    -   **errorMessage**: Error message slot for the radio group.
-   Radio Slots
    
    -   **base**: Radio root wrapper, it wraps all elements.
    -   **wrapper**: Radio wrapper, it wraps the control element.
    -   **labelWrapper**: Label and description wrapper.
    -   **label**: Label slot for the radio.
    -   **control**: Control element, it is the circle element.
    -   **description**: Description slot for the radio.

### [Custom Styles](https://nextui.org/docs/components/radio-group#custom-styles)

You can customize the `RadioGroup` and `Radio` component by passing custom Tailwind CSS classes to the component slots.

### [Custom Implementation](https://nextui.org/docs/components/radio-group#custom-implementation)

In case you need to customize the radio group even further, you can use the `useRadio` hook to create your own implementation.

## [Data Attributes](https://nextui.org/docs/components/radio-group#data-attributes)

-   RadioGroup has the following attributes on the `root` element:
    
    -   **data-orientation**: The orientation of the radio group. Based on `orientation` prop.
-   Radio has the following attributes on the `root` element:
    
    -   **data-selected**: When the radio is checked. Based on `isSelected` prop.
    -   **data-pressed**: When the radio is pressed. Based on [usePress](https://react-spectrum.adobe.com/react-aria/usePress.html).
    -   **data-invalid**: When the radio is invalid. Based on `validationState` prop.
    -   **data-readonly**: When the radio is readonly. Based on `isReadOnly` prop.
    -   **data-hover-unselected**: When the radio is being hovered and unchecked. Based on [useHover](https://react-spectrum.adobe.com/react-aria/useHover.html).
    -   **data-hover**: When the radio is being hovered. Based on [useHover](https://react-spectrum.adobe.com/react-aria/useHover.html).
    -   **data-focus**: When the radio is being focused. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
    -   **data-focus-visible**: When the radio is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
    -   **data-disabled**: When the radio is disabled. Based on `isDisabled` prop.

## [Accessibility](https://nextui.org/docs/components/radio-group#accessibility)

-   Radio groups are exposed to assistive technology via ARIA.
-   Each radio is built with a native HTML `<input>` element, which can be optionally visually hidden to allow custom styling.
-   Full support for browser features like form autofill.
-   Keyboard event support for arrows keys.
-   Keyboard focus management and cross browser normalization.
-   Group and radio labeling support for assistive technology.

## [API](https://nextui.org/docs/components/radio-group#api)

### [RadioGroup Props](https://nextui.org/docs/components/radio-group#radiogroup-props)

### [RadioGroup Events](https://nextui.org/docs/components/radio-group#radiogroup-events)

### [Radio Props](https://nextui.org/docs/components/radio-group#radio-props)