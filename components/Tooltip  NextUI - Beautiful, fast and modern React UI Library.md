Tooltips display a brief, informative message that appears when a user interacts with an element.

[Storybook](https://storybook.nextui.org/?path=/story/components-tooltip)[@nextui-org/tooltip](https://www.npmjs.com/package/@nextui-org/tooltip)[React Aria](https://react-spectrum.adobe.com/react-aria/useTooltipTrigger.html)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/tooltip)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/popover.ts)

___

[![Sponsored: Aptible](https://media.ethicalads.io/media/images/2023/08/No_Infra_Ad_1.jpg)](https://server.ethicalads.io/proxy/click/5202/9a56e6dd-807a-4318-ba54-a8a533144889/)

## [Import](https://nextui.org/docs/components/tooltip#import)

```
import {Tooltip} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/tooltip#usage)

### [With Arrow](https://nextui.org/docs/components/tooltip#with-arrow)

### [Colors](https://nextui.org/docs/components/tooltip#colors)

### [Placements](https://nextui.org/docs/components/tooltip#placements)

### [Offset](https://nextui.org/docs/components/tooltip#offset)

### [Controlled](https://nextui.org/docs/components/tooltip#controlled)

### [With Delay](https://nextui.org/docs/components/tooltip#with-delay)

You can control the `open` and `close` delay of the tooltip with `delay` and `closeDelay` props.

Hovering over the second button shows the tooltip immediately. If you wait for a delay before hovering another element, the delay restarts.

### [Custom Content](https://nextui.org/docs/components/tooltip#custom-content)

### [Custom Motion](https://nextui.org/docs/components/tooltip#custom-motion)

Tooltip offers a `motionProps` property to customize the `enter` / `exit` animation.

> Learn more about Framer motion variants [here](https://www.framer.com/motion/animation/#variants).

## [Slots](https://nextui.org/docs/components/tooltip#slots)

-   **base**: The main tooltip slot, it wraps the tooltip content.
-   **arrow**: The arrow slot, it wraps the tooltip arrow, the placement of the arrow is based on the tooltip placement, e.g. `data-[placement=top]:...`.

### [Custom Styles](https://nextui.org/docs/components/tooltip#custom-styles)

You can customize the `Tooltip` component by passing custom Tailwind CSS classes to the component slots.

## [Data Attributes](https://nextui.org/docs/components/tooltip#data-attributes)

`Tooltip` has the following attributes on the `root` element:

-   **data-open**: When the tooltip is open. Based on tooltip state.
-   **data-placement**: The placement of the tooltip. Based on `placement` prop. The arrow element is positioned based on this attribute.
-   **data-disabled**: When the tooltip is disabled. Based on `isDisabled` prop.

## [Accessibility](https://nextui.org/docs/components/tooltip#accessibility)

-   Keyboard focus management and cross browser normalization.
-   Hover management and cross browser normalization.
-   Labeling support for screen readers (aria-describedby).
-   Exposed as a tooltip to assistive technology via ARIA.
-   Matches native tooltip behavior with delay on hover of first tooltip and no delay on subsequent tooltips.

## [API](https://nextui.org/docs/components/tooltip#api)

### [Tooltip Props](https://nextui.org/docs/components/tooltip#tooltip-props)

### [Tooltip Events](https://nextui.org/docs/components/tooltip#tooltip-events)

### [Tooltip types](https://nextui.org/docs/components/tooltip#tooltip-types)

#### [Tooltip Placement](https://nextui.org/docs/components/tooltip#tooltip-placement)

```
type TooltipPlacement =  | "top"  | "bottom"  | "right"  | "left"  | "top-start"  | "top-end"  | "bottom-start"  | "bottom-end"  | "left-start"  | "left-end"  | "right-start"  | "right-end";
```

#### [Motion Props](https://nextui.org/docs/components/tooltip#motion-props)

```
export type MotionProps = HTMLMotionProps<"div">; // @see https://www.framer.com/motion/
```