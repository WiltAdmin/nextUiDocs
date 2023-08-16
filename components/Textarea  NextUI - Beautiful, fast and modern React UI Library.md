Textarea component is a multi-line Input which allows you to write large texts.

[Storybook](https://storybook.nextui.org/?path=/story/components-textarea)[@nextui-org/input](https://www.npmjs.com/package/@nextui-org/input)[React Aria](https://react-spectrum.adobe.com/react-aria/useTextField.html)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/input)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/input.ts)

___

[![Sponsored: Browserless](https://media.ethicalads.io/media/images/2023/02/Browserless_Ad_Feb_2023_JZvbtJs.png)](https://server.ethicalads.io/proxy/click/5153/155a18f4-b2b1-494e-a3e5-ef8648d4ffc7/)

## [Import](https://nextui.org/docs/components/textarea#import)

```
import {Textarea} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/textarea#usage)

### [Disabled](https://nextui.org/docs/components/textarea#disabled)

### [Readonly](https://nextui.org/docs/components/textarea#readonly)

### [Required](https://nextui.org/docs/components/textarea#required)

If you pass the `isRequired` property to the input, it will have a `danger` asterisk at the end of the label and the textarea will be required.

### [Autosize](https://nextui.org/docs/components/textarea#autosize)

Textarea grows automatically based on the content, but you can also set a min and max height to it using the `minRows` and `maxRows` properties. It is based on [react-textarea-autosize](https://github.com/Andarist/react-textarea-autosize).

### [Variants](https://nextui.org/docs/components/textarea#variants)

### [With Error Message](https://nextui.org/docs/components/textarea#with-error-message)

You can combine the `validationState="invalid"` and `errorMessage` properties to show an invalid textarea.

### [Description](https://nextui.org/docs/components/textarea#description)

### [Controlled](https://nextui.org/docs/components/textarea#controlled)

You can use the `value` and `onValueChange` properties to control the input value.

> **Note**: NextUI `Textarea` also supports native events like `onChange`, useful for form libraries such as [Formik](https://formik.org/) and [React Hook Form](https://react-hook-form.com/).

## [Slots](https://nextui.org/docs/components/textarea#slots)

-   **base**: Input wrapper, it handles alignment, placement, and general appearance.
-   **label**: Label of the textarea, it is the one that is displayed above, inside or left of the textarea.
-   **inputWrapper**: Wraps the `label` (when it is inside) and the `innerWrapper`.
-   **input**: The textarea input element.
-   **description**: The description of the textarea.
-   **errorMessage**: The error message of the textarea.

## [Data Attributes](https://nextui.org/docs/components/textarea#data-attributes)

`Textarea` has the following attributes on the `root` element:

-   **data-invalid**: When the textarea is invalid. Based on `validationState` prop.
-   **data-required**: When the textarea is required. Based on `isRequired` prop.
-   **data-readonly**: When the textarea is readonly. Based on `isReadOnly` prop.
-   **data-hover**: When the textarea is being hovered. Based on [useHover](https://react-spectrum.adobe.com/react-aria/useHover.html)
-   **data-focus**: When the textarea is being focused. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-focus-visible**: When the textarea is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-disabled**: When the textarea is disabled. Based on `isDisabled` prop.

## [Accessibility](https://nextui.org/docs/components/textarea#accessibility)

-   Built with a native `<input>` element.
-   Visual and ARIA labeling support.
-   Change, clipboard, composition, selection, and input event support.
-   Required and invalid states exposed to assistive technology via ARIA.
-   Support for description and error message help text linked to the input via ARIA.

## [API](https://nextui.org/docs/components/textarea#api)

### [Textarea Props](https://nextui.org/docs/components/textarea#textarea-props)

### [Input Events](https://nextui.org/docs/components/textarea#input-events)