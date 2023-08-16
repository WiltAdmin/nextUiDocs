Spinner express an unspecified wait time or display the length of a process.

[Storybook](https://storybook.nextui.org/?path=/story/components-spinner)[@nextui-org/spinner](https://www.npmjs.com/package/@nextui-org/spinner)[Server component](https://nextjs.org/docs/getting-started/react-essentials#server-components)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/spinner)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/spinner.ts)

___

[![Sponsored: Browserless](https://media.ethicalads.io/media/images/2023/02/Browserless_Ad_Feb_2023_JZvbtJs.png)](https://server.ethicalads.io/proxy/click/5153/155a18f4-b2b1-494e-a3e5-ef8648d4ffc7/)

## [Import](https://nextui.org/docs/components/spinner#import)

```
import {Spinner} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/spinner#usage)

> **Note**: Spinner adds `Loading` as `aria-label` by default. This is required for accessibility. You can change it by passing a `label` or `aria-label` prop.

### [Sizes](https://nextui.org/docs/components/spinner#sizes)

### [Colors](https://nextui.org/docs/components/spinner#colors)

### [With Label](https://nextui.org/docs/components/spinner#with-label)

### [Label colors](https://nextui.org/docs/components/spinner#label-colors)

## [Slots](https://nextui.org/docs/components/spinner#slots)

-   **base**: The base slot of the spinner, it wraps the circles and the label.
-   **wrapper**: The wrapper of the circles.
-   **circle1**: The first circle of the spinner.
-   **circle2**: The second circle of the spinner.
-   **label**: The label content.

## [API](https://nextui.org/docs/components/spinner#api)

### [Circular Progress Props](https://nextui.org/docs/components/spinner#circular-progress-props)

| Attribute | Type | Description | Default |
| --- | --- | --- | --- |
| label | `string` | The content to display as the label. | \- |
| size | `sm` | `md` | `lg` | The size of the spinner circles. | `md` |
| color | `default` | `primary` | `secondary` | `success` | `warning` | `danger` | The color of the spinner circles. | `primary` |
| labelColor | `default` | `primary` | `secondary` | `success` | `warning` | `danger` | The color of the spinner circles. | `default` |
| classNames | `Record<"base"｜"wrapper"｜"circle1"｜"circle2"｜"label", string>` | Allows to set custom class names for the spinner slots. | \- |