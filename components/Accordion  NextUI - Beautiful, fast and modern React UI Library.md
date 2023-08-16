Accordion display a list of high-level options that can expand/collapse to reveal more information.

[Storybook](https://storybook.nextui.org/?path=/story/components-accordion)[@nextui-org/accordion](https://www.npmjs.com/package/@nextui-org/accordion)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/accordion)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/accordion.ts)

___

[![Sponsored: Codeium](https://media.ethicalads.io/media/images/2023/05/Screen_Shot_2023-05-25_at_5.23.35_PM.png)](https://server.ethicalads.io/proxy/click/5146/02e8f7c2-075a-43b6-b28f-7838bbf80c92/)

## [Import](https://nextui.org/docs/components/accordion#import)

NextUI exports 2 accordion-related components:

-   **Accordion**: The main component to display a list of accordion items.
-   **AccordionItem**: The item component to display a single accordion item.

```
import {Accordion, AccordionItem} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/accordion#usage)

### [With Subtitle](https://nextui.org/docs/components/accordion#with-subtitle)

### [Expand multiple items](https://nextui.org/docs/components/accordion#expand-multiple-items)

If you set `selectionMode` to `multiple`, then the `Accordion` will allow multiple items to be expanded at the same time.

### [Compact](https://nextui.org/docs/components/accordion#compact)

If you set `isCompact` to `true`, the `Accordion` will be displayed in a compact style.

### [Variants](https://nextui.org/docs/components/accordion#variants)

Accordion has 4 variants: `light`, `shadow`, `bordered` and `splitted`.

#### [Light variant](https://nextui.org/docs/components/accordion#light-variant)

#### [Shadow variant](https://nextui.org/docs/components/accordion#shadow-variant)

#### [Bordered variant](https://nextui.org/docs/components/accordion#bordered-variant)

#### [Splitted variant](https://nextui.org/docs/components/accordion#splitted-variant)

### [Default expanded keys](https://nextui.org/docs/components/accordion#default-expanded-keys)

If you want to expand some items by default, you can set the `defaultExpandedKeys` property to an array of keys.

### [Disabled keys](https://nextui.org/docs/components/accordion#disabled-keys)

If you want to disable some items, you can set the `disabledKeys` property to an array of keys.

### [Start content](https://nextui.org/docs/components/accordion#start-content)

If you want to display some content before the accordion items, you can set the `startContent` property.

### [Custom Indicator](https://nextui.org/docs/components/accordion#custom-indicator)

Accordion items have a property called `indicator`. You can use it to customize the open/close indicator.

The indicator can be also a `function`, which receives the `isOpen`, `isDisabled` and the default `indicator` as parameters.

### [Custom Motion](https://nextui.org/docs/components/accordion#custom-motion)

Accordion offers a `motionProps` property to customize the `enter` / `exit` animation.

> Learn more about Framer motion variants [here](https://www.framer.com/motion/animation/#variants).

### [Controlled](https://nextui.org/docs/components/accordion#controlled)

Accordion is a controlled component, which means you need to control the `selectedKeys` property by yourself.

## [Accordion Item Slots](https://nextui.org/docs/components/accordion#accordion-item-slots)

-   **base**: The accordion item wrapper.
-   **heading**: The accordion item heading. It contains the `indicator` and the `title`.
-   **trigger**: The button that open/close the accordion item.
-   **titleWrapper**: The wrapper of the `title` and `subtitle`.
-   **title**: The accordion item title.
-   **subtitle**: The accordion item subtitle.
-   **startContent**: The content before the accordion item.
-   **indicator**: The element that indicates the open/close state of the accordion item.
-   **content**: The accordion item content.

### [Custom Accordion Styles](https://nextui.org/docs/components/accordion#custom-accordion-styles)

You can customize the accordion and accordion items styles by using any of the following properties:

-   `className`: The class name of the accordion. Modify the accordion wrapper styles.(Accordion)
-   `itemStyles`: The styles of the accordion item. Modify all accordion items styles at once. (Accordion)
-   `classNames`: The class names of the accordion items. Modify each accordion item styles separately. (AccordionItem)

Here's an example of how to customize the accordion styles:

## [Data Attributes](https://nextui.org/docs/components/accordion#data-attributes)

`AccordionItem` has the following attributes on the `root` element:

-   **data-open**: Whether the accordion item is open.
-   **data-disabled**: When the accordion item is disabled.
-   **data-hover**: When the accordion item is being hovered. Based on [useHover](https://react-spectrum.adobe.com/react-aria/useHover.html).
-   **data-focus**: When the accordion item is being focused. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-focus-visible**: When the accordion item is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-disabled**: When the accordion item is disabled. Based on `isDisabled` prop.
-   **data-pressed**: When the accordion item is pressed. Based on [usePress](https://react-spectrum.adobe.com/react-aria/usePress.html).

## [Accessibility](https://nextui.org/docs/components/accordion#accessibility)

-   Keyboard event support for Space, Enter, Arrow Up, Arrow Down and Home / End keys.
-   Keyboard focus management and cross browser normalization.
-   `aria-expanded` attribute for the accordion item.
-   `aria-disabled` attribute for the accordion item.
-   `aria-controls` attribute for the accordion item.

## [API](https://nextui.org/docs/components/accordion#api)

### [Accordion Props](https://nextui.org/docs/components/accordion#accordion-props)

### [Accordion Events](https://nextui.org/docs/components/accordion#accordion-events)

### [Accordion Item Props](https://nextui.org/docs/components/accordion#accordion-item-props)

### [Accordion Item Events](https://nextui.org/docs/components/accordion#accordion-item-events)

___

### [Types](https://nextui.org/docs/components/accordion#types)

#### [Accordion Item Indicator Props](https://nextui.org/docs/components/accordion#accordion-item-indicator-props)

```
export type AccordionItemIndicatorProps = {  /**   * The current indicator, usually an arrow icon.   */  indicator?: ReactNode;  /**   * The current open status.   */  isOpen?: boolean;  /**   * The current disabled status.   * @default false   */  isDisabled?: boolean;};type indicator?: ReactNode | ((props: AccordionItemIndicatorProps) => ReactNode) | null;
```

### [Accordion Item classNames](https://nextui.org/docs/components/accordion#accordion-item-classnames)

```
export type AccordionItemClassnames = {  base?: string;  heading?: string;  trigger?: string;  titleWrapper?: string;  title?: string;  subtitle?: string;  startContent?: string;  indicator?: string;  content?: string;};
```

#### [Motion Props](https://nextui.org/docs/components/accordion#motion-props)

```
export type MotionProps = {  /**   * If `true`, the opacity of the content will be animated   * @default true   */  animateOpacity?: boolean;  /**   * The height you want the content in its collapsed state.   * @default 0   */  startingHeight?: number;  /**   * The height you want the content in its expanded state.   * @default "auto"   */  endingHeight?: number | string;  /**   * The y-axis offset you want the content in its collapsed state.   * @default 10   */  startingY?: number;  /**   * The y-axis offset you want the content in its expanded state.   * @default 0   */  endingY?: number;} & HTMLMotionProps;
```