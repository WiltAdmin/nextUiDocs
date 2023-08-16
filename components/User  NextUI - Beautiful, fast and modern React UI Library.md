Display user information with avatar and name.

[Storybook](https://storybook.nextui.org/?path=/story/components-user)[@nextui-org/user](https://www.npmjs.com/package/@nextui-org/user)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/user)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/user.ts)

___

[![Sponsored: Aptible](https://media.ethicalads.io/media/images/2023/08/No_Infra_Ad_1.jpg)](https://server.ethicalads.io/proxy/click/5202/9a56e6dd-807a-4318-ba54-a8a533144889/)

## [Import](https://nextui.org/docs/components/user#import)

```
import {User} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/user#usage)

![Jane Doe](https://i.pravatar.cc/150?u=a04258114e29026702d)

Jane DoeProduct Designer

> **Note**: See the [Avatar](https://nextui.org/docs/components/avatar) component for more details about `avatarProps`.

### [Link Description](https://nextui.org/docs/components/user#link-description)

![Junior Garcia](https://avatars.githubusercontent.com/u/30373425?v=4)

## [Slots](https://nextui.org/docs/components/user#slots)

-   **base**: The base slot of the user, it is the main container.
-   **wrapper**: The name and description wrapper.
-   **name**: The name of the user.
-   **description**: The description of the user.

## [Data Attributes](https://nextui.org/docs/components/user#data-attributes)

`User` has the following attributes on the `root` element only when `isFocusable` is `true`:

-   **data-focus**: When the user is being focused. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html)
-   **data-focus-visible**: When the user is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html)

## [API](https://nextui.org/docs/components/user#api)

### [User Props](https://nextui.org/docs/components/user#user-props)

| Attribute | Type | Description | Default |
| --- | --- | --- | --- |
| name | `string` | The name of the user. | \- |
| description | `ReactNode` | The description component. | \- |
| isFocusable | `boolean` | Whether the user is focusable. This is useful when using `Dropdown` or similar components. | `false` |
| avatarProps | [AvatarProps](https://nextui.org/docs/components/avatar#avatar-props) | The avatar component props. The `name` is passed by default. | \- |
| classNames | `Record<"base"｜ "wrapper"｜ "name"｜ "description", string>` | Allows to set custom class names for the user slots. | \- |