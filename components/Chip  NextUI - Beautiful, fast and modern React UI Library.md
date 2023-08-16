A Chip is a small block of essential information that represent an input, attribute, or action.

[Storybook](https://storybook.nextui.org/?path=/story/components-chip)[@nextui-org/chip](https://www.npmjs.com/package/@nextui-org/chip)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/chip)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/chip.ts)

___

[![Sponsored: MongoDB](https://media.ethicalads.io/media/images/2022/08/EA-2_240x180.png)](https://server.ethicalads.io/proxy/click/5096/f4edfdc6-113d-4991-9c21-569f801c8b75/)

## [Import](https://nextui.org/docs/components/chip#import)

```
import {Chip} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/chip#usage)

### [Disabled](https://nextui.org/docs/components/chip#disabled)

### [Sizes](https://nextui.org/docs/components/chip#sizes)

### [Colors](https://nextui.org/docs/components/chip#colors)

Default

Primary

Secondary

Success

Warning

Danger

### [Radius](https://nextui.org/docs/components/chip#radius)

### [Variants](https://nextui.org/docs/components/chip#variants)

Solid

Bordered

Light

Flat

Faded

Shadow

Dot

### [Start & End Content](https://nextui.org/docs/components/chip#start--end-content)

### [With Close Button](https://nextui.org/docs/components/chip#with-close-button)

If you pass the `onClose` prop, the close button will be visible. You can override t he close icon by passing the `endContent` prop.

### [With Avatar](https://nextui.org/docs/components/chip#with-avatar)

![JW](https://i.pravatar.cc/300?u=a042581f4e29026709d)Avatar

JAvatar

### [List of Chips](https://nextui.org/docs/components/chip#list-of-chips)

Apple

Banana

Cherry

Watermelon

Orange

## [Slots](https://nextui.org/docs/components/chip#slots)

-   **base**: The base slot of the chip, it is the container of the chip.
-   **content**: The content slot of the chip, it is the container of the chip children.
-   **dot**: Small dot on the left side of the chip. It is visible when the `variant=dot` prop is passed.
-   **avatar**: Avatar classes of the chip. It is visible when the `avatar` prop is passed.
-   **closeButton**: Close button classes of the chip. It is visible when the `onClose` prop is passed.

### [Custom Styles](https://nextui.org/docs/components/chip#custom-styles)

You can customize the `Chip` component by passing custom Tailwind CSS classes to the component slots.

## [API](https://nextui.org/docs/components/chip#api)

### [Chip Props](https://nextui.org/docs/components/chip#chip-props)

| Attribute | Type | Description | Default |
| --- | --- | --- | --- |
| children | `ReactNode` | The content of the chip. | \- |
| variant | `solid` | `bordered` | `light` | `flat` | `faded` | `shadow` | `ghost` | The chip appearance style. | `solid` |
| color | `default` | `primary` | `secondary` | `success` | `warning` | `danger` | The color of the chip. | `default` |
| size | `sm` | `md` | `lg` | The size of the chip. | `md` |
| radius | `none` | `sm` | `md` | `lg` | `full` | The radius of the chip. | `full` |
| avatar | `ReactNode` | Avatar to be rendered in the left side of the chip. | \- |
| startContent | `ReactNode` | Element to be rendered in the left side of the chip. This prop overrides the `avatar` prop. | \- |
| endContent | `ReactNode` | Element to be rendered in the right side of the chip. This prop overrides the default close button when `onClose` is passed. | \- |
| isDisabled | `boolean` | Whether the chip is disabled. | `false` |
| classNames | `Record<"base"｜ "content"｜ "dot"｜ "avatar"｜ "closeButton", string>` | Allows to set custom class names for the chip slots. | \- |

### [Chip Events](https://nextui.org/docs/components/chip#chip-events)

| Attribute | Type | Description |
| --- | --- | --- |
| onClose | `(e: PressEvent) => void` | Handler that is called when the close button is pressed. If you pass this prop, the chip will display a close button (endContent). |