Popover is a **non-modal** dialog that floats around its disclosure. It's commonly used for displaying additional rich content on top of something.

[Storybook](https://storybook.nextui.org/?path=/story/components-popover)[@nextui-org/popover](https://www.npmjs.com/package/@nextui-org/popover)[React Aria](https://react-spectrum.adobe.com/react-aria/usePopover.html)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/popover)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/popover.ts)

___

[![Sponsored: Aptible](https://media.ethicalads.io/media/images/2023/08/Logo_Ad_2.jpg)](https://server.ethicalads.io/proxy/click/5201/8fe8aed7-c1e0-4dd7-a5f6-aba193455ece/)

## [Import](https://nextui.org/docs/components/popover#import)

NextUI exports 3 popover-related components:

-   **Popover**: The main component to display a popover.
-   **PopoverTrigger**: The component that triggers the popover.
-   **PopoverContent**: The component that contains the popover content.

```
import {Popover, PopoverTrigger, PopoverContent} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/popover#usage)

### [With Arrow](https://nextui.org/docs/components/popover#with-arrow)

### [Colors](https://nextui.org/docs/components/popover#colors)

### [Placements](https://nextui.org/docs/components/popover#placements)

### [Offset](https://nextui.org/docs/components/popover#offset)

### [Controlled](https://nextui.org/docs/components/popover#controlled)

### [Title Props](https://nextui.org/docs/components/popover#title-props)

To be sure that the popover exposes the correct title to assistive technologies, you should use the `titleProps` prop on the `PopoverContent` component. To use this prop, you must pass a function as a child.

### [With Form](https://nextui.org/docs/components/popover#with-form)

The `Popover` handles the focus within the popover content. It means that you can use the popover with form elements without any problem. the focus returns to the trigger when the popover closes.

> **Note**: You can add the `autoFocus` prop to the first `Input` component to focus it when the popover opens.

### [Backdrop](https://nextui.org/docs/components/popover#backdrop)

The `Popover` component has a `backdrop` prop to show a backdrop behind the popover. The backdrop can be either `transparent`, `opaque` or `blur`. The default value is `transparent`.

### [Custom Motion](https://nextui.org/docs/components/popover#custom-motion)

Popover offers a `motionProps` property to customize the `enter` / `exit` animation.

> Learn more about Framer motion variants [here](https://www.framer.com/motion/animation/#variants).

### [Custom Trigger](https://nextui.org/docs/components/popover#custom-trigger)

## [Slots](https://nextui.org/docs/components/popover#slots)

-   **base**: The main popover slot, it wraps the popover content.
-   **trigger**: The popover trigger slot, it has small styles to ensure the trigger works correctly.
-   **backdrop**: The backdrop slot, it contains the backdrop styles.
-   **arrow**: The arrow slot, it wraps the popover arrow, the placement of the arrow is based on the popover placement, e.g. `data-[placement=top]:...`.

### [Custom Styles](https://nextui.org/docs/components/popover#custom-styles)

You can customize the `Popover` component by passing custom Tailwind CSS classes to the component slots.

## [Data Attributes](https://nextui.org/docs/components/popover#data-attributes)

`Popover` has the following attributes on the `PopoverContent` element:

-   **data-open**: When the popover is open. Based on popover state.
-   **data-placement**: The placement of the popover. Based on `placement` prop. The arrow element is positioned based on this attribute.
-   **data-focus**: When the popover is being focused. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-focus-visible**: When the popover is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).

## [Accessibility](https://nextui.org/docs/components/popover#accessibility)

-   The trigger and popover are automatically associated semantically via ARIA.
-   Content outside the popover is hidden from assistive technologies while it is open.
-   The popover closes when interacting outside, or pressing the Escape key.
-   Focus is moved into the popover on mount, and restored to the trigger element on unmount.
-   The popover is positioned relative to the trigger element, and automatically flips and adjusts to avoid overlapping with the edge of the browser window.
-   Scrolling is prevented outside the popover to avoid unintentionally repositioning or closing it.

## [API](https://nextui.org/docs/components/popover#api)

### [Popover Props](https://nextui.org/docs/components/popover#popover-props)

### [Popover Events](https://nextui.org/docs/components/popover#popover-events)

### [PopoverTrigger Props](https://nextui.org/docs/components/popover#popovertrigger-props)

### [PopoverContent Props](https://nextui.org/docs/components/popover#popovercontent-props)

### [Popover types](https://nextui.org/docs/components/popover#popover-types)

#### [Popover Placement](https://nextui.org/docs/components/popover#popover-placement)

```
type PopoverPlacement =  | "top"  | "bottom"  | "right"  | "left"  | "top-start"  | "top-end"  | "bottom-start"  | "bottom-end"  | "left-start"  | "left-end"  | "right-start"  | "right-end";
```

#### [Motion Props](https://nextui.org/docs/components/popover#motion-props)

```
export type MotionProps = HTMLMotionProps<"div">; // @see https://www.framer.com/motion/
```