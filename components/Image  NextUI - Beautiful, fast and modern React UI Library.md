The Image component is used to display images with support for fallback.

[Storybook](https://storybook.nextui.org/?path=/story/components-image)[@nextui-org/image](https://www.npmjs.com/package/@nextui-org/image)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/image)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/image.ts)

___

[![Sponsored: MongoDB](https://media.ethicalads.io/media/images/2022/08/EA-2_240x180.png)](https://server.ethicalads.io/proxy/click/5096/f4edfdc6-113d-4991-9c21-569f801c8b75/)

## [Import](https://nextui.org/docs/components/image#import)

```
import {Image} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/image#usage)

### [Blurred](https://nextui.org/docs/components/image#blurred)

You can use the `isBlurred` prop to duplicate the image and blur it to create a blurred effect.

### [Zoomed](https://nextui.org/docs/components/image#zoomed)

You can use the `isZoomed` prop make the image zoomed when hovered.

### [Animated Loading](https://nextui.org/docs/components/image#animated-loading)

Image component has a built-in `skeleton` animation to indicate the image is loading and an `opacity` animation when the image loads.

> **Note**: The `URL` uses `https://app.requestly.io/delay` to simulate a slow network.

### [Image with fallback](https://nextui.org/docs/components/image#image-with-fallback)

You can use the `fallbackSrc` prop to display a fallback image when:

-   The `fallbackSrc` prop is provided.
-   The image provided in `src` is still loading.
-   The image provided in `src` fails to load.
-   The image provided in `src` is not found.

### [With Next.js Image](https://nextui.org/docs/components/image#with-nextjs-image)

Next.js provides an optimized [Image](https://nextjs.org/docs/app/api-reference/components/image) component, you can use it with NextUI `Image` component as well.

> **Note**: NextUI's `Image` component is `client-side`, using hooks like `useState` for loading states and animations. Use Next.js `Image` alone if these features aren't required.

## [Slots](https://nextui.org/docs/components/image#slots)

-   **img**: Slot for the image element.
-   **wrapper**: Image wrapper, it handles alignment, placement, and general appearance.
-   **zoomedWrapper**: The wrapper slot for the zoomed image it avoids the image content to overflow the parent container.
-   **blurredImg**: The wrapper slot for the duplicated blurred image.

## [API](https://nextui.org/docs/components/image#api)

### [Image Props](https://nextui.org/docs/components/image#image-props)

### [Image Events](https://nextui.org/docs/components/image#image-events)