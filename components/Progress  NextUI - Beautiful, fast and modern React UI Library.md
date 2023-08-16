The Progress component allows you to view the progress of any activity.

[Storybook](https://storybook.nextui.org/?path=/story/components-progress)[@nextui-org/progress](https://www.npmjs.com/package/@nextui-org/progress)[React Aria](https://react-spectrum.adobe.com/react-aria/useProgressBar.html)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/progress)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/progress.ts)

___

[![Sponsored: Aptible](https://media.ethicalads.io/media/images/2023/08/Logo_Ad_2.jpg)](https://server.ethicalads.io/proxy/click/5201/8fe8aed7-c1e0-4dd7-a5f6-aba193455ece/)

## [Import](https://nextui.org/docs/components/progress#import)

```
import {Progress} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/progress#usage)

> **Note**: Make sure to pass the `aria-label` prop when the `label` prop is not provided. This is required for accessibility.

### [Sizes](https://nextui.org/docs/components/progress#sizes)

### [Colors](https://nextui.org/docs/components/progress#colors)

### [Indeterminate](https://nextui.org/docs/components/progress#indeterminate)

You can use the `isIndeterminate` prop to display an indeterminate progress bar. This is useful when you don't know how long an operation will take.

### [Striped](https://nextui.org/docs/components/progress#striped)

### [With Label](https://nextui.org/docs/components/progress#with-label)

> **Note**: If you pass the `label` prop you don't need to pass `aria-label` prop anymore.

### [With Value](https://nextui.org/docs/components/progress#with-value)

### [Value Formatting](https://nextui.org/docs/components/progress#value-formatting)

Values are formatted as a percentage by default, but this can be modified by using the `formatOptions` prop to specify a different format. `formatOptions` is compatible with the option parameter of [Intl.NumberFormat](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/NumberFormat) and is applied based on the current locale.

## [Slots](https://nextui.org/docs/components/progress#slots)

-   **base**: The base slot of the progress, it is the main container.
-   **labelWrapper**: The label and value label wrapper.
-   **label**: The label of the progress.
-   **value**: The value label of the progress.
-   **track**: The track is the background bar of the progress.
-   **indicator**: The indicator is the bar that is filled according to the `value`.

### [Custom Styles](https://nextui.org/docs/components/progress#custom-styles)

You can customize the `Progress` component by passing custom Tailwind CSS classes to the component slots.

## [Data Attributes](https://nextui.org/docs/components/progress#data-attributes)

`CircularProgress` has the following attributes on the `root` element:

-   **data-indeterminate**: Indicates whether the progress is indeterminate.
-   **data-disabled**: Indicates whether the progress is disabled. Based on `isDisabled` prop.

## [Accessibility](https://nextui.org/docs/components/progress#accessibility)

-   Exposed to assistive technology as a progress bar via ARIA.
-   Labeling support for accessibility.
-   Internationalized number formatting as a percentage or value.
-   Determinate and indeterminate progress support.
-   Exposes the `aria-valuenow`, `aria-valuemin`, `aria-valuemax` and `aria-valuetext` attributes.

## [API](https://nextui.org/docs/components/progress#api)

### [Circular Progress Props](https://nextui.org/docs/components/progress#circular-progress-props)