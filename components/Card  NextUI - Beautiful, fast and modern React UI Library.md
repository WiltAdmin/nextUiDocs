Card is a container for text, photos, and actions in the context of a single subject.

[Storybook](https://storybook.nextui.org/?path=/story/components-card)[@nextui-org/card](https://www.npmjs.com/package/@nextui-org/card)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/card)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/card.ts)

___

[![Sponsored: Codeium](https://media.ethicalads.io/media/images/2023/05/Screen_Shot_2023-05-25_at_5.23.35_PM.png)](https://server.ethicalads.io/proxy/click/5146/02e8f7c2-075a-43b6-b28f-7838bbf80c92/)

## [Import](https://nextui.org/docs/components/card#import)

NextUI exports 4 card-related components:

-   **Card**: The main component to display a card.
-   **CardHeader**: Commonly used for the title of a card.
-   **CardBody**: The content of the card.
-   **CardFooter**: Commonly used for actions.

```
import {Card, CardHeader, CardBody, CardFooter} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/card#usage)

### [With Divider](https://nextui.org/docs/components/card#with-divider)

> See the [Divider](https://nextui.org/docs/components/divider) component for more details.

### [With Image](https://nextui.org/docs/components/card#with-image)

You can pass the `isFooterBlurred` prop to the card to blur the footer.

### [Composition](https://nextui.org/docs/components/card#composition)

You can use other NextUI components inside the card to compose a more complex card.

### [Blurred Card](https://nextui.org/docs/components/card#blurred-card)

You can pass the `isBlurred` prop to the card to blur the card.

### [Primary Action](https://nextui.org/docs/components/card#primary-action)

If you pass the `isPressable` prop to the card, it will be rendered as a button.

> **Note**: that the used callback function is `onPress` instead of `onClick`. Please see the [usePress](https://react-spectrum.adobe.com/react-aria/usePress.html#usepress) component for more details.

### [Cover Image](https://nextui.org/docs/components/card#cover-image)

You can use `Image` component as the cover of the card by taking it out of the `CardBody` component.

## [Data Attributes](https://nextui.org/docs/components/card#data-attributes)

`Card` has the following attributes on the `root` element:

-   **data-hover**: When the card is being hovered. Based on [useHover](https://react-spectrum.adobe.com/react-aria/useHover.html)
-   **data-focus**: When the card is being focused. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-focus-visible**: When the card is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-disabled**: When the card is disabled. Based on `isDisabled` prop.
-   **data-pressed**: When the card is pressed. Based on [usePress](https://react-spectrum.adobe.com/react-aria/usePress.html)

## [API](https://nextui.org/docs/components/card#api)

### [Card Props](https://nextui.org/docs/components/card#card-props)

### [Card Events](https://nextui.org/docs/components/card#card-events)