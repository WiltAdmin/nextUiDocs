The Pagination component allows you to display active page and navigate between multiple pages.

[Storybook](https://storybook.nextui.org/?path=/story/components-pagination)[@nextui-org/pagination](https://www.npmjs.com/package/@nextui-org/pagination)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/pagination)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/pagination.ts)

___

[![Sponsored: Browserless](https://media.ethicalads.io/media/images/2023/02/Browserless_Ad_Feb_2023.png)](https://server.ethicalads.io/proxy/click/5152/364b3784-ddb1-4fcf-9c8d-fa07a7f600ea/)

## [Import](https://nextui.org/docs/components/pagination#import)

NextUI exports 3 pagination-related components:

-   **Pagination**: The main component to display a pagination.
-   **PaginationItem**: The internal component to display a pagination item.
-   **PaginationCursor**: The internal item component to display the current page.

```
import {Pagination, PaginationItem, PaginationCursor} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/pagination#usage)

### [Disabled](https://nextui.org/docs/components/pagination#disabled)

### [Sizes](https://nextui.org/docs/components/pagination#sizes)

### [Colors](https://nextui.org/docs/components/pagination#colors)

## [Data Attributes](https://nextui.org/docs/components/pagination#data-attributes)

`Pagination` has the following attributes on the `root` element:

-   **data-controls**: Indicates whether the pagination has controls. Based on `showControls` prop.
-   **data-loop**: When the pagination is looped. Based on `loop` prop.
-   **data-dots-jump**: Indicates whether the pagination has dots jump. Based on `dotsJump` prop.
-   **data-total**: The total number of pages. Based on `total` prop.
-   **data-active-page**: The active page. Based on `activePage` prop.

## [Accessibility](https://nextui.org/docs/components/pagination#accessibility)

-   The root node has a role of `navigation` by default.
-   The pagination items have an aria-label that identifies the item purpose ("next page button", "previous page button", etc.), you can override this label by using the `getItemAriaLabel` function.
-   The pagination items are in tab order, with a tabindex of "0".

## [API](https://nextui.org/docs/components/pagination#api)

___

### [Types](https://nextui.org/docs/components/pagination#types)

```
export type PaginationItemRenderProps = {  // The pagination item ref.  ref?: Ref<T>;  // The pagination item value.  value: PaginationItemValue;  // The pagination item index.  index: number;  // The active page number.  activePage: number;  // Whether the pagination item is active.  isActive: boolean;  // Whether the pagination item is the first item in the pagination.  isFirst: boolean;  // Whether the pagination item is the last item in the pagination.  isLast: boolean;  // Whether the pagination item is the next item in the pagination.  isNext: boolean;  // Whether the pagination item is the previous item in the pagination.  isPrevious: boolean;  // The pagination item className.  className: string;  // Callback to go to the next page.  onNext: () => void;  // Callback to go to the previous page.  onPrevious: () => void;  // Callback to go to the page.  setPage: (page: number) => void;};type renderItem?: (props: PaginationItemRenderProps) => ReactNode;
```