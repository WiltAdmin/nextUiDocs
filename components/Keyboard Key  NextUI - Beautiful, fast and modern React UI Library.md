Keyboard key is a component to display which key or combination of keys performs a given action.

[Storybook](https://storybook.nextui.org/?path=/story/components-kbd)[@nextui-org/kbd](https://www.npmjs.com/package/@nextui-org/kbd)[Server component](https://nextjs.org/docs/getting-started/react-essentials#server-components)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/kbd)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/kbd.ts)

___

[![Sponsored: Browserless](https://media.ethicalads.io/media/images/2023/02/Browserless_Ad_Feb_2023.png)](https://server.ethicalads.io/proxy/click/5152/364b3784-ddb1-4fcf-9c8d-fa07a7f600ea/)

## [Import](https://nextui.org/docs/components/kbd#import)

```
import {Kbd} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/kbd#usage)

### [Keys](https://nextui.org/docs/components/kbd#keys)

> **Note**: Check the [API](https://nextui.org/docs/components/kbd#keyboard-keys) section to see all available keys.

## [Slots](https://nextui.org/docs/components/kbd#slots)

-   **base**: Kbd wrapper, it handles alignment, placement, and general appearance.
-   **abbr**: The `keys` wrapper that handles the appearance of the keys.
-   **content**: The children wrapper that handles the appearance of the content.

## [Accessibility](https://nextui.org/docs/components/kbd#accessibility)

-   Each command `key` has a `title` attribute that describes the action that the key performs.

## [API](https://nextui.org/docs/components/kbd#api)

### [Keyboard Key Props](https://nextui.org/docs/components/kbd#keyboard-key-props)

### [Keyboard Keys](https://nextui.org/docs/components/kbd#keyboard-keys)

List of supported keys.

```
type KbdKey =  | "command"  | "shift"  | "ctrl"  | "option"  | "enter"  | "delete"  | "escape"  | "tab"  | "capslock"  | "up"  | "right"  | "down"  | "left"  | "pageup"  | "pagedown"  | "home"  | "end"  | "help"  | "space";
```