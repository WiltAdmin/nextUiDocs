Tables are used to display tabular data using rows and columns. They allow users to quickly scan, sort, compare, and take action on large amounts of data.

[Storybook](https://storybook.nextui.org/?path=/story/components-table)[@nextui-org/table](https://www.npmjs.com/package/@nextui-org/table)[Source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/components/table)[Styles source](https://github.com/nextui-org/nextui/tree/feat/v2/packages/core/theme/src/components/table.ts)

___

[![Sponsored: Browserless](https://media.ethicalads.io/media/images/2023/02/Browserless_Ad_Feb_2023_JZvbtJs.png)](https://server.ethicalads.io/proxy/click/5153/155a18f4-b2b1-494e-a3e5-ef8648d4ffc7/)

## [Import](https://nextui.org/docs/components/table#import)

NextUI exports 6 table-related components:

-   **Table**: The main component to display a table.
-   **TableHeader**: The header of the table.
-   **TableBody**: The body of the table.
-   **TableColumn**: The column of the table.
-   **TableRow**: The row of the table.
-   **TableCell**: The cell of the table.

```
import {  Table,  TableHeader,  TableBody,  TableColumn,  TableRow,  TableCell} from "@nextui-org/react";
```

## [Usage](https://nextui.org/docs/components/table#usage)

### [Dynamic](https://nextui.org/docs/components/table#dynamic)

To render a table dynamically, you can use the `columns` prop to pass the columns and `items` prop to pass the data.

#### [Why not array map?](https://nextui.org/docs/components/table#why-not-array-map)

Using the `items` prop and providing a render function allows [react-aria](https://react-spectrum.adobe.com/react-aria/index.html) to automatically cache the results of rendering each item and avoid re-rendering all items in the collection when only one of them changes. This has big performance benefits for large collections.

You could also use `Array.map` to render the items, but it will not be as performant as using the `items` and `columns` prop.

Example:

```
import {Table, TableHeader, TableColumn, TableBody, TableRow, TableCell, getKeyValue} from "@nextui-org/react";const rows = [...];const columns = [...];export default function App() {  return (    <Table aria-label="Example table with dynamic content">      <TableHeader>        {columns.map((column) =>          <TableColumn key={column.key}>{column.label}</TableColumn>        )}      </TableHeader>      <TableBody>        {rows.map((row) =>          <TableRow key={row.key}>            {(columnKey) => <TableCell>{getKeyValue(row, columnKey)}</TableCell>}          </TableRow>        )}      </TableBody>    </Table>  );}
```

> **Note**: To learn more about React Aria collections and how to use them, please check [React Aria Collections](https://react-spectrum.adobe.com/react-stately/collections.html).

### [Empty State](https://nextui.org/docs/components/table#empty-state)

You can use the `emptyContent` prop to render a custom component when the table is empty.

In case you don't want to render the header, you can use the `hideHeader` prop.

### [Without Wrapper](https://nextui.org/docs/components/table#without-wrapper)

By default the table is wrapped in a `div` element with a small shadow effect and a border radius. You can use the `removeWrapper` prop to remove the wrapper and only render the table.

### [Custom Cells](https://nextui.org/docs/components/table#custom-cells)

You can render any component inside the table cell. In the example below, we are rendering different components according to the `key` of the column.

### [Striped Rows](https://nextui.org/docs/components/table#striped-rows)

You can use the `isStriped` prop to render striped rows.

### [Single Row Selection](https://nextui.org/docs/components/table#single-row-selection)

It is possible to make the table rows selectable. To do so, you can use the `selectioMode` prop. Use `defaultSelectedKeys` to provide a default set of selected rows.

> **Note**: The value of the selected keys must match the key prop of the row.

### [Multiple Row Selection](https://nextui.org/docs/components/table#multiple-row-selection)

You can also select multiple rows by using the `selectionMode="multiple"` prop. Use `defaultSelectedKeys` to provide a default set of selected rows.

> **Note**: When using multiple selection, selectable checkboxes will be rendered in the first column of the table.

### [Disallow Empty Selection](https://nextui.org/docs/components/table#disallow-empty-selection)

Table also supports a `disallowEmptySelection` prop which forces the user to have at least one row in the Table selected at all times. In this mode, if a single row is selected and the user presses it, it will not be deselected.

### [Controlled Selection](https://nextui.org/docs/components/table#controlled-selection)

To programmatically control row selection, use the `selectedKeys` prop paired with the `onSelectionChange` callback. The key prop from the selected rows will be passed into the callback when the row is pressed, allowing you to update state accordingly.

> **Note**: The `selectedKeys` property must be an `Set` object.

### [Disabled Rows](https://nextui.org/docs/components/table#disabled-rows)

You can disable rows by using the `disabledKeys` prop. This will prevent rows from being selectable as shown in the example below.

### [Selection Behavior](https://nextui.org/docs/components/table#selection-behavior)

By default, Table uses the `toggle` selection behavior, which behaves like a checkbox group: clicking, tapping, or pressing the Space or Enter keys toggles selection for the focused row.

When the `selectionBehavior` prop is set to `replace`, clicking a row with the mouse replaces the selection with only that row. Using the arrow keys moves both focus and selection. To select multiple rows, modifier keys such as Ctrl, Cmd, and Shift can be used.

### [Rows Actions](https://nextui.org/docs/components/table#rows-actions)

Table supports rows via the `onRowAction` callback. In the default `toggle` selection behavior, when nothing is selected, clicking or tapping the row triggers the row action.

This behavior is slightly different in the `replace` selection behavior, where single clicking selects the row and actions are performed via double click.

### [Sorting Rows](https://nextui.org/docs/components/table#sorting-rows)

Table supports sorting its data when a column header is pressed. To designate that a `Column` should support sorting, provide it with the `allowsSorting` prop.

Table accepts a `sortDescriptor` prop that defines the current column key to sort by and the sort direction (ascending/descending). When the user presses a sortable column header, the column's key and sort direction is passed into the `onSortChange` callback, allowing you to update the `sortDescriptor` appropriately.

We recommend using the `useAsyncList` hook from [@react-stately/data](https://react-spectrum.adobe.com/react-stately/useAsyncList.html) to manage the data sorting. So make sure to install it before using the sorting feature.

```
npm install @react-stately/data
```

```
import {useAsyncList} from "@react-stately/data";
```

> Note that we passed the `isLoading` and `loadingContent` props to `TableBody` to render a loading state while the data is being fetched.

### [Loading more data](https://nextui.org/docs/components/table#loading-more-data)

Table allows you to add a custom component at the end of the table, on the example below we are using a button to load more data.

> **Note**: We passed the `isHeaderSticky` to the `Table` component to make the header sticky.

### [Paginated Table](https://nextui.org/docs/components/table#paginated-table)

You can use the [Pagination](https://nextui.org/components/pagination) component to paginate the table.

It is also possible to use the [Pagination](https://nextui.org/components/pagination) component to paginate the table asynchronously. To fetch the data, we are using the `useAsyncList` hook from [@react-stately/data](https://react-spectrum.adobe.com/react-stately/useAsyncList.html). Please check the installation instructions in the [Sorting Rows](https://nextui.org/docs/components/table#sorting-rows) section.

Table also supports infinite pagination. To do so, you can use the `useAsyncList` hook from [@react-stately/data](https://react-spectrum.adobe.com/react-stately/useAsyncList.html) and [@nextui-org/use-infinite-scroll](https://www.npmjs.com/package/@nextui-org/use-infinite-scroll) hook.

### [Use Case Example](https://nextui.org/docs/components/table#use-case-example)

When creating a table, you usually need core functionalities like sorting, pagination, and filtering. In the example below, we combined all these functionalities to create a complete table.

## [Slots](https://nextui.org/docs/components/table#slots)

-   **base**: Defines a flexible column layout and relative positioning for the table component.
-   **wrapper**: Applies to the outermost wrapper, providing padding, flexible layout, relative positioning, visual styles, and scrollable overflow handling.
-   **table**: Sets the table to have a full minimum width and auto-adjusting height.
-   **thead**: Specifies rounded corners for the first child row in the table header.
-   **tbody**: No specific styles are applied to the body of the table.
-   **tr**: Styles for table rows including group focus, outline properties, and a set of undefined focus-visible classes.
-   **th**: Styles for table headers, including padding, text alignment, font properties, and special styles for sortable columns.
-   **td**: Applies to table cells, with properties for padding, alignment, and relative positioning, plus special styles for first child elements, selection indication, and disabled cells.
-   **tfoot**: No specific styles are applied to the footer of the table.
-   **sortIcon**: Styles for sorting icons, with properties for margin, opacity, and transition effects based on sorting direction and hover state.
-   **emptyWrapper**: Defines style for an empty table, with text alignment, color, and a specified height.
-   **loadingWrapper**: Style applied when the table is loading, positioning it centrally in its container.

### [Custom Styles](https://nextui.org/docs/components/table#custom-styles)

You can customize the `Table` component by passing custom Tailwind CSS classes to the component slots.

## [Data Attributes](https://nextui.org/docs/components/table#data-attributes)

`TableBody` has the following attributes:

-   **data-empty**: When the table is empty.
-   **data-loading**: When the table data is loading. Based on `TableBody` `isLoading` and `loadingContent` props.

`TableRow` has the following attributes:

-   **data-selected**: When the row is selected. Based on `Table` `selectedKeys` prop.
-   **data-disabled**: When the row is disabled. Based on `Table` `disabledKeys` prop.
-   **data-hover**: When the row is being hovered. Based on [useHover](https://react-spectrum.adobe.com/react-aria/useHover.html)
-   **data-focus-visible**: When the row is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).
-   **data-first**: When the row is the first row.
-   **data-middle**: When the row is in the middle.
-   **data-odd**: When the row is odd.
-   **data-last**: When the row is the last row.

`TableCell` has the following attributes:

-   **data-selected**: When the cell row is selected. Based on `Table` `selectedKeys` prop.
-   **data-focus-visible**: When the cell is being focused with the keyboard. Based on [useFocusRing](https://react-spectrum.adobe.com/react-aria/useFocusRing.html).

## [Accessibility](https://nextui.org/docs/components/table#accessibility)

-   Exposed to assistive technology as a grid using ARIA.
-   Keyboard navigation between columns, rows, cells, and in-cell focusable elements via the arrow keys.
-   Single, multiple, or no row selection via mouse, touch, or keyboard interactions.
-   Support for disabled rows, which cannot be selected.
-   Column sorting support.
-   Async loading, infinite scrolling, filtering, and sorting support.
-   Support for both toggle and replace selection behaviors.
-   Labeling support for accessibility.
-   Ensures that selections are announced using an ARIA live region.
-   Support for marking columns as row headers, which will be read when navigating the rows with a screen reader.
-   Optional support for checkboxes in each row for selection, as well as in the header to select all rows.
-   Automatic scrolling support during keyboard navigation.
-   Support for row actions via double click, Enter key, or tapping.
-   Typeahead to allow focusing rows by typing text.
-   Long press to enter selection mode on touch when there is both selection and row actions.

## [API](https://nextui.org/docs/components/table#api)

### [Table Props](https://nextui.org/docs/components/table#table-props)

### [Table Events](https://nextui.org/docs/components/table#table-events)

#### [TableColumn Props](https://nextui.org/docs/components/table#tablecolumn-props)

#### [TableBody Props](https://nextui.org/docs/components/table#tablebody-props)

### [TableBody Events](https://nextui.org/docs/components/table#tablebody-events)

#### [TableRow Props](https://nextui.org/docs/components/table#tablerow-props)

#### [TableCell Props](https://nextui.org/docs/components/table#tablecell-props)

___

### [Table types](https://nextui.org/docs/components/table#table-types)

#### [Sort descriptor](https://nextui.org/docs/components/table#sort-descriptor)

```
type SortDescriptor = {  column: React.Key;  direction: "ascending" | "descending";};
```

#### [Selection](https://nextui.org/docs/components/table#selection)

```
type Selection = "all" | Set<React.Key>;
```

#### [Loading state](https://nextui.org/docs/components/table#loading-state)

```
type LoadingState = "loading" | "sorting" | "loadingMore" | "error" | "idle" | "filtering";
```