Circular progress indicators are utilized to indicate an undetermined wait period or visually represent the duration of a process.

```
import {CircularProgress} from "@nextui-org/react";
```

Values are formatted as a percentage by default, but this can be modified by using the `formatOptions` prop to specify a different format. `formatOptions` is compatible with the option parameter of [Intl.NumberFormat](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/NumberFormat) and is applied based on the current locale.

You can customize the `CircularProgress` component by passing custom Tailwind CSS classes to the component slots.