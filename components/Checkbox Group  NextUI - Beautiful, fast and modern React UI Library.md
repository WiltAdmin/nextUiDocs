A CheckboxGroup allows users to select one or more items from a list of choices.

[Storybook](https://storybook.nextui.org/?path=/story/components-checkboxgroup)[@nextui-org/checkbox](https://www.npmjs.com/package/@nextui-org/checkbox)[React Aria](https://react-spectrum.adobe.com/react-aria/useCheckboxGroup.html)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/checkbox)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/checkbox.ts)

___

[![Sponsored: MongoDB](https://media.ethicalads.io/media/images/2022/08/EA-2_240x180.png)](https://server.ethicalads.io/proxy/click/5096/f4edfdc6-113d-4991-9c21-569f801c8b75/)

## [Import](https://nextui.org/docs/components/checkbox-group#import)

NextUI exports 2 checkbox-related components:

-   **CheckboxGroup**: The root component, it wraps the label and the wrapper.
-   **Checkbox**: The checkbox component.

```
import {CheckboxGroup, Checkbox} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/checkbox-group#usage)

Select cities

Buenos AiresSydneySan FranciscoLondonTokyo

### [Disabled](https://nextui.org/docs/components/checkbox-group#disabled)

Select cities

Buenos AiresSydneySan FranciscoLondonTokyo

### [Horizontal](https://nextui.org/docs/components/checkbox-group#horizontal)

Select cities

Buenos AiresSydneySan FranciscoLondonTokyo

### [Controlled](https://nextui.org/docs/components/checkbox-group#controlled)

You can use the `value` and `onValueChange` properties to control the checkbox input value.

Select cities

Buenos AiresSydneySan Francisco

Selected: buenos-aires, sydney

## [Slots](https://nextui.org/docs/components/checkbox-group#slots)

-   **base**: Checkbox group root wrapper, it wraps the label and the wrapper.
-   **wrapper**: Checkbox group wrapper, it wraps all checkboxes.
-   **label**: Checkbox group label, it is placed before the wrapper.
-   **description**: The description of the checkbox group.
-   **errorMessage**: The error message of the checkbox group.

### [Custom Styles](https://nextui.org/docs/components/checkbox-group#custom-styles)

You can customize the `CheckboxGroup` component by passing custom Tailwind CSS classes to the component slots.

Select employees

![Junior Garcia](https://avatars.githubusercontent.com/u/30373425?v=4)

![John Doe](https://i.pravatar.cc/300?u=a042581f4e29026707d)

![Zoey Lang](https://i.pravatar.cc/300?u=a042581f4e29026704d)

Technical Writer

Out of office

![William Howard](https://i.pravatar.cc/300?u=a048581f4e29026701d)

Selected:

### [Custom Implementation](https://nextui.org/docs/components/checkbox-group#custom-implementation)

In case you need to customize the checkbox even further, you can use the `useCheckboxGroup` hook to create your own implementation.

Select amenities

Wifi

TV

Kitchen

Parking

Pool

Gym

Selected:

> **Note**: We used [Tailwind Variants](https://www.tailwind-variants.org/) to implement the styles above, you can use any other library such as [clsx](https://www.npmjs.com/package/clsx) to achieve the same result.

## [API](https://nextui.org/docs/components/checkbox-group#api)

### [Checkbox Group Props](https://nextui.org/docs/components/checkbox-group#checkbox-group-props)

| Attribute | Type | Description | Default |
| --- | --- | --- | --- |
| children | `ReactNode[]` | `ReactNode[]` | The checkboxes items. | \- |
| orientation | `vertical` | `horizontal` | The axis the checkbox group items should align with. | `vertical` |
| color | `default` | `primary` | `secondary` | `success` | `warning` | `danger` | The color of the checkboxes. | `primary` |
| size | `xs` | `sm` | `md` | `lg` | `xl` | The size of the checkboxes. | `md` |
| radius | `none` | `base` | `xs` | `sm` | `md` | `lg` | `xl` | `full` | The radius of the checkboxes. | `md` |
| name | `string` | The name of the CheckboxGroup, used when submitting an HTML form. | \- |
| value | `string[]` | The current selected values. (controlled). | \- |
| lineThrough | `boolean` | Whether the checkboxes label should be crossed out. | `false` |
| defaultValue | `string[]` | The default selected values. (uncontrolled). | \- |
| validationState | `valid` | `invalid` | Whether the inputs should display its "valid" or "invalid" visual styling. | `false` |
| description | `ReactNode` | The checkbox group description. | \- |
| errorMessage | `ReactNode` | The checkbox group error message. | \- |
| isDisabled | `boolean` | Whether the checkbox group is disabled. | `false` |
| isRequired | `boolean` | Whether user checkboxes are required on the input before form submission. | `false` |
| isReadOnly | `boolean` | Whether the checkboxes can be selected but not changed by the user. | \- |
| disableAnimation | `boolean` | Whether the animation should be disabled. | `false` |
| classNames | `Record<"base"｜ "wrapper"｜ "label", string>` | Allows to set custom class names for the checkbox group slots. | \- |

### [Checkbox Group Events](https://nextui.org/docs/components/checkbox-group#checkbox-group-events)

| Attribute | Type | Description |
| --- | --- | --- |
| onChange | `((value: string[]) => void)` | Handler that is called when the value changes. |