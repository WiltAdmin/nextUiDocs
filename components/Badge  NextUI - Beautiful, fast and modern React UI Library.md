Badges are used as a small numerical value or status descriptor for UI elements.

[Storybook](https://storybook.nextui.org/?path=/story/components-badge)[@nextui-org/badge](https://www.npmjs.com/package/@nextui-org/badge)[Server component](https://nextjs.org/docs/getting-started/react-essentials#server-components)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/badge)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/badge.ts)

___

[![Sponsored: Codeium](https://media.ethicalads.io/media/images/2023/05/Screen_Shot_2023-05-25_at_5.23.35_PM.png)](https://server.ethicalads.io/proxy/click/5146/02e8f7c2-075a-43b6-b28f-7838bbf80c92/)

## [Import](https://nextui.org/docs/components/badge#import)

```
import {Badge} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/badge#usage)

![avatar](https://i.pravatar.cc/300?u=a042581f4e29026709d)5

### [Sizes](https://nextui.org/docs/components/badge#sizes)

### [Colors](https://nextui.org/docs/components/badge#colors)

### [Variants](https://nextui.org/docs/components/badge#variants)

### [Placements](https://nextui.org/docs/components/badge#placements)

### [Shapes](https://nextui.org/docs/components/badge#shapes)

For a better positioning, you can use the `shape` property to define the shape of the badge.

![avatar](https://i.pravatar.cc/150?u=a042f81f4e29026024d)5

![avatar](https://i.pravatar.cc/150?u=a04258a2462d826712d)5

### [Badge Visibility](https://nextui.org/docs/components/badge#badge-visibility)

You can control the visibility of the badge by using the `isInvisible` property.

### [Content Examples](https://nextui.org/docs/components/badge#content-examples)

### [Disable Outline](https://nextui.org/docs/components/badge#disable-outline)

By default, the badge has an outline, you can disable it by using the `disableOutline` property.

![avatar](https://i.pravatar.cc/150?u=a042f81f4e29026024d)5

![avatar](https://i.pravatar.cc/150?u=a04258a2462d826712d)5

### [Accessibility](https://nextui.org/docs/components/badge#accessibility)

It's not advisable to depend on the badge's content for accurate announcement. Instead, consider supplying a comprehensive description, such as using `aria-label`.

## [API](https://nextui.org/docs/components/badge#api)

### [Badge Props](https://nextui.org/docs/components/badge#badge-props)

| Attribute | Type | Description | Default |
| --- | --- | --- | --- |
| children \* | `ReactNode` | The wrapped component. | \- |
| content | `string` | `number` | `ReactNode` | The content of the badge. The badge will be rendered relative to its children. | \- |
| variant | `solid` | `flat` | `faded` | `shadow` | The variant style of the badge. | `solid` |
| color | `default` | `primary` | `secondary` | `success` | `warning` | `danger` | The color of the badge. | `default` |
| size | `sm` | `md` | `lg` | The size of the badge. | `md` |
| shape | `circle` | `rectangle` | The shape of the badge. | `rectangle` |
| placement | `top-right` | `top-left` | `bottom-right` | `bottom-left` | The placement of the badge. | `top-right` |
| disableOutline | `boolean` | If `true`, the badge will not have an outline. | `false` |
| disableAnimation | `boolean` | If `true`, the badge will not have an animation. | `false` |
| isInvisible | `boolean` | If `true`, the badge will be invisible. | `false` |
| isOneChar | `boolean` | If `true`, the badge will have the same width and height. | `false` |
| isDot | `boolean` | If `true`, the badge will have smaller dimensions. | `false` |
| classNames | `Record<"base"｜"badge", string>` | Allows to set custom class names for the badge slots. | \- |