The Avatar component is used to represent a user, and displays the profile picture, initials or fallback icon.

[Storybook](https://storybook.nextui.org/?path=/story/components-avatar)[@nextui-org/avatar](https://www.npmjs.com/package/@nextui-org/avatar)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/avatar)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/avatar.ts)

___

[![Sponsored: Codeium](https://media.ethicalads.io/media/images/2023/05/Screen_Shot_2023-05-25_at_5.23.35_PM.png)](https://server.ethicalads.io/proxy/click/5146/02e8f7c2-075a-43b6-b28f-7838bbf80c92/)

## [Import](https://nextui.org/docs/components/avatar#import)

NextUI exports 3 avatar-related components:

-   **Avatar**: The main component to display an avatar.
-   **AvatarGroup**: A wrapper component to display a group of avatars.
-   **AvatarIcon**: The default icon used as fallback when the image fails to load.

```
import {Avatar, AvatarGroup, AvatarIcon} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/avatar#usage)

### [Sizes](https://nextui.org/docs/components/avatar#sizes)

### [Disabled](https://nextui.org/docs/components/avatar#disabled)

### [Bordered](https://nextui.org/docs/components/avatar#bordered)

### [Radius](https://nextui.org/docs/components/avatar#radius)

### [Colors](https://nextui.org/docs/components/avatar#colors)

### [Avatar Fallbacks](https://nextui.org/docs/components/avatar#avatar-fallbacks)

If there is an error loading the `src` of the avatar, there are 2 fallbacks:

-   If there's a `name` prop, we use it to generate the initials and a random, accessible background color.
-   If there's no `name` prop, we use a default avatar.

If the `showFallback` is not passed, the fallbacks will not be displayed.

### [Custom Fallback](https://nextui.org/docs/components/avatar#custom-fallback)

You can also provide a custom fallback component to be displayed when the `src` fails to load.

### [Custom Implementation](https://nextui.org/docs/components/avatar#custom-implementation)

In case you need to customize the avatar even further, you can use the `useAvatar` hook to create your own implementation.

### [Custom intials logic](https://nextui.org/docs/components/avatar#custom-intials-logic)

It is possible to customize the logic used to generate the initials by passing a function to the `getInitials` prop. By default we merge the first characters of each word in the `name` prop.

## [Avatar Group](https://nextui.org/docs/components/avatar#avatar-group)

### [Group Disabled](https://nextui.org/docs/components/avatar#group-disabled)

### [Group Max Count](https://nextui.org/docs/components/avatar#group-max-count)

You can limit the number of avatars displayed by passing the `max` prop to the `AvatarGroup` component.

### [Group Total Count](https://nextui.org/docs/components/avatar#group-total-count)

You can display the total number of avatars by passing the `total` prop to the `AvatarGroup` component.

### [Group Custom count](https://nextui.org/docs/components/avatar#group-custom-count)

NextUI provides a `renderCount` prop to customize the count displayed when the `total` prop is passed.

### [Group Grid](https://nextui.org/docs/components/avatar#group-grid)

By passing the `isGrid` prop to the `AvatarGroup` component, the avatars will be displayed in a grid layout.

### [Group Custom Implementation](https://nextui.org/docs/components/avatar#group-custom-implementation)

In case you need to customize the avatar group even further, you can use the `useAvatarGroup` hook and the `AvatarGroupProvider` to create your own implementation.

## [Slots](https://nextui.org/docs/components/avatar#slots)

-   **base**: Avatar wrapper, it includes styles for focus ring, position, and general appearance.
-   **img**: Image element within the avatar, it includes styles for opacity transition and size.
-   **fallback**: Fallback content when the image fails to load or is not provided, it includes styles for centering the content.
-   **name**: Initials displayed when the image is not provided or fails to load, it includes styles for font, text alignment, and inheritance.
-   **icon**: Icon element within the avatar, it includes styles for centering the content, text inheritance, and size.

### [Custom Avatar Styles](https://nextui.org/docs/components/avatar#custom-avatar-styles)

You can customize any part of the avatar by using the `classNames` prop, each `slot` has its own `className`.

## [Data Attributes](https://nextui.org/docs/components/avatar#data-attributes)

`Avatar` has the following attributes on the `root` element:

-   **data-hover**: When the avatar is being hovered. Based on [useHover](https://react-spectrum.adobe.com/react-aria/useHover.html)
-   **data-focus**: When the avatar is being focused. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html), it is applied when `isFocusable` is `true` or when the `as` property is assigned as `button`.
-   **data-focus-visible**: When the avatar is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html), it is applied when `isFocusable` is `true` or when the `as` property is assigned as `button`.

## [API](https://nextui.org/docs/components/avatar#api)

### [Avatar Props](https://nextui.org/docs/components/avatar#avatar-props)

### [Avatar Group Props](https://nextui.org/docs/components/avatar#avatar-group-props)