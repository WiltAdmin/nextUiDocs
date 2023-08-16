Skeleton is a placeholder to show a loading state and the expected shape of a component.

[Storybook](https://storybook.nextui.org/?path=/story/components-skeleton)[@nextui-org/skeleton](https://www.npmjs.com/package/@nextui-org/skeleton)[Server component](https://nextjs.org/docs/getting-started/react-essentials#server-components)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/skeleton)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/skeleton.ts)

___

[![Sponsored: Aptible](https://media.ethicalads.io/media/images/2023/08/Logo_Ad_2.jpg)](https://server.ethicalads.io/proxy/click/5201/8fe8aed7-c1e0-4dd7-a5f6-aba193455ece/)

## [Import](https://nextui.org/docs/components/skeleton#import)

```
import {Skeleton} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/skeleton#usage)

### [Standalone](https://nextui.org/docs/components/skeleton#standalone)

Skeleton takes the shape of its `children` component by default, but you can also use it as a standalone component.

### [Loaded State](https://nextui.org/docs/components/skeleton#loaded-state)

You can use the `isLoaded` prop to stop the skeleton animation and show the children component.

## [Slots](https://nextui.org/docs/components/skeleton#slots)

-   **base**: The base slot of the skeleton, it contains the `before` and `after` pseudo elements to create the animation.
-   **content**: The wrapped component to show the skeleton shape. It is visible only when the `isLoaded` prop is `true`.

## [Data Attributes](https://nextui.org/docs/components/skeleton#data-attributes)

`Skeleton` has the following attributes on the `root` element:

-   **data-loaded**: Indicates the loaded state of the skeleton. Based on the `isLoaded` prop.

## [API](https://nextui.org/docs/components/skeleton#api)

### [Skeleton Props](https://nextui.org/docs/components/skeleton#skeleton-props)

| Attribute | Type | Description | Default |
| --- | --- | --- | --- |
| children | `ReactNode` | The content of the skeleton. | \- |
| isLoaded | `boolean` | Whether the skeleton is loaded. | `false` |
| disableAnimation | `boolean` | Whether to disable the animations. | `false` |
| classNames | `Record<"base"｜"content", string>` | Allows to set custom class names for the skeleton slots. | \- |