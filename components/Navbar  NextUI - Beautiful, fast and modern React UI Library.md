A responsive navigation header positioned on top side of your page that includes support for branding, links, navigation, collapse menu and more.

[Storybook](https://storybook.nextui.org/?path=/story/components-navbar)[@nextui-org/navbar](https://www.npmjs.com/package/@nextui-org/navbar)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/navbar)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/navbar.ts)

___

[![Sponsored: Browserless](https://media.ethicalads.io/media/images/2023/02/Browserless_Ad_Feb_2023.png)](https://server.ethicalads.io/proxy/click/5152/364b3784-ddb1-4fcf-9c8d-fa07a7f600ea/)

## [Import](https://nextui.org/docs/components/navbar#import)

NextUI exports 7 navbar-related components:

-   **Navbar**: The main component of navbar.
-   **NavbarBrand**: The component for branding.
-   **NavbarContent**: The component for wrapping navbar items.
-   **NavbarItem**: The component for navbar item.
-   **NavbarMenuToggle**: The component for toggling navbar menu.
-   **NavbarMenu**: The component for wrapping navbar menu items.
-   **NavbarMenuItem**: The component for navbar menu item.

```
import {  Navbar,   NavbarBrand,   NavbarContent,   NavbarItem,   NavbarMenuToggle,  NavbarMenu,  NavbarMenuItem} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/navbar#usage)

### [Static](https://nextui.org/docs/components/navbar#static)

You can use the `position` prop to make the navbar static positioned (the default behavior is `sticky`).

### [Hide on scroll](https://nextui.org/docs/components/navbar#hide-on-scroll)

It is possible to hide the navbar on scroll by using the `shouldHideOnScroll` prop.

You can use the `NavbarMenuToggle` and `NavbarMenu` components to display a togglable menu.

If you want to remove the `open` / `close` animation, you can pass the `disableAnimation={true}` prop to `Navbar` component.

You can use the `isMenuOpen` and `onMenuOpenChange` props to control the navbar menu state.

### [With Border](https://nextui.org/docs/components/navbar#with-border)

You can use the `isBordered` prop to add a bottom border to the navbar.

### [Disabling Blur](https://nextui.org/docs/components/navbar#disabling-blur)

Navbar has a blur effect by default. You can disable it by using the `isBlurred=false` prop.

It is possible to use the [Dropdown](https://nextui.org/docs/components/dropdown) component to display a dropdown menu as navbar item.

### [With Avatar](https://nextui.org/docs/components/navbar#with-avatar)

Example of a navbar with avatar and dropdown menu.

### [With Search Input](https://nextui.org/docs/components/navbar#with-search-input)

Example of a navbar with search input.

### [Customizing the active item](https://nextui.org/docs/components/navbar#customizing-the-active-item)

When the `NavbarItem` is active, it will have a `data-active` attribute. You can use this attribute to customize it.

## [Slots](https://nextui.org/docs/components/navbar#slots)

-   **base**: The main slot for the navbar. It takes the full width of the parent and wraps the navbar elements including the menu.
-   **wrapper**: The slot that contains the navbar elements such as `brand`, `content` and `toggle`.
-   **brand**: The slot for the `NavbarBrand` component.
-   **content**: The slot for the `NavbarContent` component.
-   **item**: The slot for the `NavbarItem` component.
-   **toggle**: The slot for the `NavbarMenuToggle` component.
-   **toggleIcon**: The slot for the `NavbarMenuToggle` icon.
-   **menu**: The slot for the `NavbarMenu` component.
-   **menuItem**: The slot for the `NavbarMenuItem` component.

## [Data Attributes](https://nextui.org/docs/components/navbar#data-attributes)

`Navbar` has the following attributes on the `root` element:

-   **data-menu-open**: Indicates if the navbar menu is open.
-   **data-hidden**: Indicates if the navbar is hidden. It is used when the `shouldHideOnScroll` prop is `true`.

`NavbarContent`

-   **data-justify**: The justify content of the navbar content. It takes into account the correct space distribution.

`NavbarItem` has the following attributes on the `root` element:

-   **data-active**: Indicates if the navbar item is active. It is used when the `isActive` prop is `true`.

`NavbarMenuToggle` has the following attributes on the `root` element:

-   **data-open**: Indicates if the navbar menu is open. It is used when the `isMenuOpen` prop is `true`.
-   **data-pressed**: When the navbar menu toggle is pressed. Based on [usePress](https://react-spectrum.adobe.com/react-aria/usePress.html)
-   **data-hover**: When the navbar menu toggle is being hovered. Based on [useHover](https://react-spectrum.adobe.com/react-aria/useHover.html)
-   **data-focus-visible**: When the navbar menu toggle is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).

## [API](https://nextui.org/docs/components/navbar#api)

### [Navbar Props](https://nextui.org/docs/components/navbar#navbar-props)

### [Navbar Events](https://nextui.org/docs/components/navbar#navbar-events)

### [NavbarContent Props](https://nextui.org/docs/components/navbar#navbarcontent-props)

### [NavbarItem Props](https://nextui.org/docs/components/navbar#navbaritem-props)

> **Note**: The rest of the navbar components such as `NavbarMenuItem` and `NavbarBrand` have the same props as the `li` element.

### [Navbar types](https://nextui.org/docs/components/navbar#navbar-types)

#### [Motion Props](https://nextui.org/docs/components/navbar#motion-props)

```
export type MotionProps = HTMLMotionProps<"div">; // @see https://www.framer.com/motion/
```