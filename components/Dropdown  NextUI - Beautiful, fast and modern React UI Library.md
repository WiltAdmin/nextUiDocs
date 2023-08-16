Displays a list of actions or options that a user can choose.

[Storybook](https://storybook.nextui.org/?path=/story/components-dropdown)[@nextui-org/dropdown](https://www.npmjs.com/package/@nextui-org/dropdown)[React Aria](https://react-spectrum.adobe.com/react-aria/useMenu.html)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/dropdown)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/dropdown.ts)

___

[![Sponsored: MongoDB](https://media.ethicalads.io/media/images/2022/08/EA-2_240x180.png)](https://server.ethicalads.io/proxy/click/5096/f4edfdc6-113d-4991-9c21-569f801c8b75/)

## [Import](https://nextui.org/docs/components/dropdown#import)

NextUI exports 5 dropdown-related components:

-   **Dropdown**: The main component, which is a wrapper for the other components. This component is an extension of the [Popover](https://nextui.org/docs/components/popover) component, so it accepts all the props of the Popover component.
-   **DropdownTrigger**: The component that triggers the dropdown menu to open.
-   **DropdownMenu**: The component that contains the dropdown items.
-   **DropdownSection**: The component that contains a group of dropdown items.
-   **DropdownItem**: The component that represents a dropdown item.

```
import {  Dropdown,  DropdownTrigger,  DropdownMenu,  DropdownSection,  DropdownItem} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/dropdown#usage)

### [Dynamic items](https://nextui.org/docs/components/dropdown#dynamic-items)

Dropdown follows the [Collection Components API](https://react-spectrum.adobe.com/react-stately/collections.html), accepting both static and dynamic collections.

-   **Static**: The usage example above shows the static implementation, which can be used when the full list of options is known ahead of time.
-   **Dynamic**: The example below can be used when the options come from an external data source such as an API call, or update over time.

### [Disabled Keys](https://nextui.org/docs/components/dropdown#disabled-keys)

Dropdown items can be disabled using the `disabledKeys` prop to the `DropdownMenu` component.

> **Note**: It's important to have a unique key for each item, otherwise the disabled keys will not work.

### [Action event](https://nextui.org/docs/components/dropdown#action-event)

You can use the `onAction` prop to get the key of the selected item.

### [Variants](https://nextui.org/docs/components/dropdown#variants)

You can use the `variant` in the `DropdownMenu` component to change the `hover` style of the dropdown items.

### [Single Selection](https://nextui.org/docs/components/dropdown#single-selection)

You can set the `selectionMode` property as `single` to allow the user to select only one item at a time.

### [Multiple Selection](https://nextui.org/docs/components/dropdown#multiple-selection)

You can set the `selectionMode` property as `multiple` to allow the user to select multiple items at a time.

### [With Shortcut](https://nextui.org/docs/components/dropdown#with-shortcut)

You can use the `shortcut` prop to add a shortcut to the dropdown item.

> **Note**: Dropdown does not handle the shortcut event, you need to handle it yourself.

### [With Icons](https://nextui.org/docs/components/dropdown#with-icons)

It is possible to add icons to the dropdown items using the `startContent` / `endContent` props.

> **Note**: Note: If you use `currentColor` as the icon color, the icon will have the same color as the item text.

### [With Description](https://nextui.org/docs/components/dropdown#with-description)

You can use the `description` prop to add a description to the dropdown item.

### [With Sections](https://nextui.org/docs/components/dropdown#with-sections)

You can use the `DropdownSection` component to group dropdown items.

> **Note**: Sections without a `title` must provide an `aria-label` for accessibility.

### [Custom Trigger](https://nextui.org/docs/components/dropdown#custom-trigger)

You can use any component as a trigger for the dropdown menu, just wrap it in the `DropdownTrigger` component.

### [Changing the backdrop](https://nextui.org/docs/components/dropdown#changing-the-backdrop)

As we mentioned earlier, the `Dropdown` component is an extension of the [Popover](https://nextui.org/docs/components/popover) component, so it accepts all the props of the Popover component, including the `backdrop` prop.

## [Slots](https://nextui.org/docs/components/dropdown#slots)

Dropdown has 2 components with slots the `DropdownItem` and `DropdownSection` components.

### [DropdownItem](https://nextui.org/docs/components/dropdown#dropdownitem)

-   **base**: The main slot for the dropdown item. It wraps all the other slots.
-   **wrapper**: The `title` and `description` wrapper.
-   **title**: The title of the dropdown item.
-   **description**: The description of the dropdown item.
-   **shortcut**: The shorcut slot.
-   **selectedIcon**: The selected icon slot. This is only visible when the item is selected.

### [DropdownSection](https://nextui.org/docs/components/dropdown#dropdownsection)

-   **base**: The main slot for the dropdown section. It wraps all the other slots.
-   **heading**: The title that is render on top of the section group.
-   **group**: The group of dropdown items.
-   **divider**: The divider that is render between the groups. This is only visible when `showDivider` is `true`.

### [Customizing the dropdown popover](https://nextui.org/docs/components/dropdown#customizing-the-dropdown-popover)

The `Dropdown` component is an extension of the [Popover](https://nextui.org/docs/components/popover) component, so you can use the same slots to customize the dropdown.

### [Customizing the dropdown items style](https://nextui.org/docs/components/dropdown#customizing-the-dropdown-items-style)

You can customize the dropdown items either by using the `DropdownMenu` `itemClasses` prop or by using the `DropdownItem` slots, the `itemClasses` allows you to customize all the items at once, while the slots allow you to customize each item individually.

### [Keyboard Interactions](https://nextui.org/docs/components/dropdown#keyboard-interactions)

## [Data Attributes](https://nextui.org/docs/components/dropdown#data-attributes)

`DropdownItem` has the following attributes on the `root` element:

-   **data-disabled**: When the dropdown item is disabled. Based on dropdown `disabledKeys` prop.
-   **data-selected**: When the dropdown item is selected. Based on dropdown `selectedKeys` prop.
-   **data-hover**: When the dropdown item is being hovered. Based on [useHover](https://react-spectrum.adobe.com/react-aria/useHover.html)
-   **data-pressed**: When the dropdown item is pressed. Based on [usePress](https://react-spectrum.adobe.com/react-aria/usePress.html)
-   **data-focus**: When the dropdown item is being focused. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-focus-visible**: When the dropdown item is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).

## [Accessibility](https://nextui.org/docs/components/dropdown#accessibility)

-   Exposed to assistive technology as a button with a menu using ARIA.
-   Support for single, multiple, or no selection.
-   Support for disabled items.
-   Support for sections.
-   Complex item labeling support for accessibility.
-   Keyboard navigation support including arrow keys, home/end, page up/down. See [Keyboard Interactions](https://nextui.org/docs/components/dropdown#keyboard-interactions) for more details.
-   Automatic scrolling support during keyboard navigation.
-   Keyboard support for opening the menu using the arrow keys, including automatically focusing the first or last item accordingly.
-   Typeahead to allow focusing items by typing text.
-   Virtualized scrolling support for performance with long lists.

## [API](https://nextui.org/docs/components/dropdown#api)

### [Dropdown Props](https://nextui.org/docs/components/dropdown#dropdown-props)

### [Dropdown Events](https://nextui.org/docs/components/dropdown#dropdown-events)

___

### [DropdownTrigger Props](https://nextui.org/docs/components/dropdown#dropdowntrigger-props)

___

___

### [DropdownSection Props](https://nextui.org/docs/components/dropdown#dropdownsection-props)

___

### [DropdownItem Props](https://nextui.org/docs/components/dropdown#dropdownitem-props)

### [DropdownItem Events](https://nextui.org/docs/components/dropdown#dropdownitem-events)

___

### [Types](https://nextui.org/docs/components/dropdown#types)

#### [Dropdown Item Selected Icon Props](https://nextui.org/docs/components/dropdown#dropdown-item-selected-icon-props)

```
export type DropdownItemSelectedIconProps = {  /**   * The current icon, usually an checkmark icon.   */  icon?: ReactNode;  /**   * The current selected status.   */  isSelected?: boolean;  /**   * The current disabled status.   * @default false   */  isDisabled?: boolean;};type selectedIcon?: ReactNode | ((props: DropdownItemSelectedIconProps) => ReactNode) | null;
```