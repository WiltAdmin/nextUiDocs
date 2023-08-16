Displays a dialog with a custom content that requires attention or provides additional information.

[Storybook](https://storybook.nextui.org/?path=/story/components-modal)[@nextui-org/modal](https://www.npmjs.com/package/@nextui-org/modal)[React Aria](https://react-spectrum.adobe.com/react-aria/useModal.html)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/modal)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/modal.ts)

___

[![Sponsored: Browserless](https://media.ethicalads.io/media/images/2023/02/Browserless_Ad_Feb_2023.png)](https://server.ethicalads.io/proxy/click/5152/364b3784-ddb1-4fcf-9c8d-fa07a7f600ea/)

## [Import](https://nextui.org/docs/components/modal#import)

NextUI exports 5 modal-related components:

-   **Modal**: The main component to display a modal.
-   **ModalContent**: The wrapper of the other modal components.
-   **ModalHeader**: The header of the modal.
-   **ModalBody**: The body of the modal.
-   **ModalFooter**: The footer of the modal.

```
import {  Modal,   ModalContent,   ModalHeader,   ModalBody,   ModalFooter} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/modal#usage)

When the modal opens:

-   Focus is bounded within the modal and set to the first tabbable element.
-   Content behind a modal dialog is inert, meaning that users cannot interact with it.

### [Sizes](https://nextui.org/docs/components/modal#sizes)

### [Non-dissmissable](https://nextui.org/docs/components/modal#non-dissmissable)

By default the modal can be closed by clicking on the overlay or pressing the Esc key. You can disable this behavior by setting the `isDismissable` prop to `false`.

### [Modal placement](https://nextui.org/docs/components/modal#modal-placement)

By default the modal is centered on screens higher than `sm` and is at the `bottom` of the screen on mobile. This placement is called `auto`, but you can change it by using the `placement` prop.

> **Note**: The `top-center` and `bottom-center` positions mean that the modal is positioned at the top / bottom of the screen on mobile and at the center of the screen on desktop.

### [Overflow scroll](https://nextui.org/docs/components/modal#overflow-scroll)

You can use the `scrollBehavior` prop to set the scroll behavior of the modal.

-   **inside**: The modal content will be scrollable.
-   **outside**: The modal content will be scrollable and the modal will be fixed.

### [With Form](https://nextui.org/docs/components/modal#with-form)

The `Modal` handles the focus within the modal content. It means that you can use the modal with form elements without any problem. the focus returns to the trigger when the modal closes.

> **Note**: You can add the `autoFocus` prop to the first `Input` component to focus it when the modal opens.

### [Backdrop](https://nextui.org/docs/components/modal#backdrop)

The `Modal` component has a `backdrop` prop to show a backdrop behind the modal. The backdrop can be either `transparent`, `opaque` or `blur`. The default value is `transparent`.

### [Custom Backdrop](https://nextui.org/docs/components/modal#custom-backdrop)

You can customize the backdrop by using the `backdrop` slot.

### [Custom Motion](https://nextui.org/docs/components/modal#custom-motion)

Modal offers a `motionProps` property to customize the `enter` / `exit` animation.

> Learn more about Framer motion variants [here](https://www.framer.com/motion/animation/#variants).

## [Slots](https://nextui.org/docs/components/modal#slots)

-   **wrapper**: The wrapper slot of the modal. It wraps the `base` and the `backdrop` slots.
-   **base**: The main slot of the modal content.
-   **backdrop**: The backdrop slot, it is displayed behind the modal.
-   **header**: The header of the modal, it is displayed at the top of the modal.
-   **body**: The body of the modal, it is displayed in the middle of the modal.
-   **footer**: The footer of the modal, it is displayed at the bottom of the modal.
-   **closeButton**: The close button of the modal.

### [Custom Styles](https://nextui.org/docs/components/modal#custom-styles)

You can customize the `Modal` component by passing custom Tailwind CSS classes to the component slots.

## [Data Attributes](https://nextui.org/docs/components/modal#data-attributes)

`Modal` has the following attributes on the `root` element:

-   **data-open**: When the modal is open. Based on modal state.
-   **data-dismissable**: When the modal is dismissable. Based on `isDismissable` prop.

## [Accessibility](https://nextui.org/docs/components/modal#accessibility)

-   Content outside the modal is hidden from assistive technologies while it is open.
-   The modal optionally closes when interacting outside, or pressing the Esc key.
-   Focus is moved into the modal on mount, and restored to the trigger element on unmount.
-   While open, focus is contained within the modal, preventing the user from tabbing outside.
-   Scrolling the page behind the modal is prevented while it is open, including in mobile browsers.

## [API](https://nextui.org/docs/components/modal#api)

### [Modal Props](https://nextui.org/docs/components/modal#modal-props)

### [Modal Events](https://nextui.org/docs/components/modal#modal-events)

### [Modal types](https://nextui.org/docs/components/modal#modal-types)

#### [Motion Props](https://nextui.org/docs/components/modal#motion-props)

```
export type MotionProps = HTMLMotionProps<"div">; // @see https://www.framer.com/motion/
```