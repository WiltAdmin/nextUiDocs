Tabs organize content into multiple sections and allow users to navigate between them.

[Storybook](https://storybook.nextui.org/?path=/story/components-tabs)[@nextui-org/tabs](https://www.npmjs.com/package/@nextui-org/tabs)[React Aria](https://react-spectrum.adobe.com/react-aria/useTabList.html)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/tabs)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/tabs.ts)

___

[![Sponsored: Browserless](https://media.ethicalads.io/media/images/2023/02/Browserless_Ad_Feb_2023_JZvbtJs.png)](https://server.ethicalads.io/proxy/click/5153/155a18f4-b2b1-494e-a3e5-ef8648d4ffc7/)

## [Import](https://nextui.org/docs/components/tabs#import)

NextUI exports 2 tabs-related components:

-   **Tabs**: The main component to display a tab list.
-   **Tab**: The component to display a tab item. The children of this component will be displayed as the content of the tab.

```
import {Tabs, Tab} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/tabs#usage)

### [Dynamic](https://nextui.org/docs/components/tabs#dynamic)

You can render tabs dynamically by using `items` prop.

### [Disabled](https://nextui.org/docs/components/tabs#disabled)

### [Disabled Item](https://nextui.org/docs/components/tabs#disabled-item)

### [Sizes](https://nextui.org/docs/components/tabs#sizes)

### [Radius](https://nextui.org/docs/components/tabs#radius)

### [Colors](https://nextui.org/docs/components/tabs#colors)

### [Variants](https://nextui.org/docs/components/tabs#variants)

### [With Icons](https://nextui.org/docs/components/tabs#with-icons)

### [Controlled](https://nextui.org/docs/components/tabs#controlled)

You can use the `onSelectionChange` and `selectedKey` props to control the selected tab.

### [With Form](https://nextui.org/docs/components/tabs#with-form)

## [Slots](https://nextui.org/docs/components/tabs#slots)

-   **base**: The main tabs slot, it wraps the items and the panels.
-   **tabList**: The tab list slot, it wraps the tab items.
-   **tab**: The tab slot, it wraps the tab item.
-   **tabContent**: The tab content slot, it wraps the tab content.
-   **cursor**: The cursor slot, it wraps the cursor. This is only visible when `disableAnimation=false`
-   **panel**: The panel slot, it wraps the tab panel (content).

### [Custom Styles](https://nextui.org/docs/components/tabs#custom-styles)

You can customize the `Tabs` component by passing custom Tailwind CSS classes to the component slots.

## [Data Attributes](https://nextui.org/docs/components/tabs#data-attributes)

`Tab` has the following attributes on the `root` element:

-   **data-selected**: When the tab is selected.
-   **data-disabled**: When the tab is disabled.
-   **data-hover**: When the tab is being hovered. Based on [useHover](https://react-spectrum.adobe.com/react-aria/useHover.html).
-   **data-hover-selected**: When the tab is being hovered and is not selected. Based on [useHover](https://react-spectrum.adobe.com/react-aria/useHover.html) and `selected` state.
-   **data-focus**: When the tab is being focused. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-focus-visible**: When the tab is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-pressed**: When the tab is pressed. Based on [usePress](https://react-spectrum.adobe.com/react-aria/usePress.html).

## [Accessibility](https://nextui.org/docs/components/tabs#accessibility)

-   Support for mouse, touch, and keyboard interactions on tabs.
-   Keyboard event support for arrows keys.
-   Support for disabled tabs.
-   Follows the tabs ARIA pattern, semantically linking tabs and their associated tab panels.
-   Focus management for tab panels without any focusable children.

## [API](https://nextui.org/docs/components/tabs#api)

### [Tabs Props](https://nextui.org/docs/components/tabs#tabs-props)

### [Tabs Events](https://nextui.org/docs/components/tabs#tabs-events)

### [Tab Props](https://nextui.org/docs/components/tabs#tab-props)

#### [Motion Props](https://nextui.org/docs/components/tabs#motion-props)

```
export type MotionProps = HTMLMotionProps<"div">; // @see https://www.framer.com/motion/
```