# Empty State

The `<EmptyState>` component is an element that can be used as a placeholder when no data is present (such as an empty list, or a placeholder page for future content). This is only used when no data is available, rather than during loading (see [empty states pattern](https://pxblue.github.io/patterns/empty-states)).

<img width="500" alt="Empty state with all props" src="./images/emptyState.png">

## Usage

```tsx
import { EmptyState, wrapIcon } from '@pxblue/react-native-components';
import _Battery from '@pxblue/icons-svg/battery.svg';
const Battery = wrapIcon({ IconClass: _Battery });
...
<EmptyState
    title={'Nothing Found'}
    description={'Not a single thing'}
    IconClass={Battery}
/>
```

## API

<div style="overflow: auto">

| Prop Name   | Description                            | Type                                               | Required | Default |
| ----------- | -------------------------------------- | -------------------------------------------------- | -------- | ------- |
| title       | The main text to display               | `string`                                           | yes      |         |
| description | The secondary text to display          | `string`                                           | no       |         |
| IconClass   | The primary icon                       | `React.Component<{ size: number, color: string }>` | no       |         |
| IconProps   | Props to pass through to the icon      | `{ size?: number, color?: string }`                | no       |         |
| iconSize    | The size of the primary icon (100-200) | `number`                                           | no       | 100     |
| iconColor   | The color of the primary icon          | `string`                                           | no       | `text`  |
| actions     | Additional components to render below  | `JSX.Element`                                      | no       |         |
| theme       | Theme partial for default styling      | `Theme`                                            | no       |         |

</div>

### Styles

You can override the internal styles used by PX Blue by passing a `styles` prop. It supports the following keys:

| Name  | Description                         |
| ----- | ----------------------------------- |
| root  | Styles applied to the root element  |
| units | Styles applied to the units element |
| value | Styles applied to the value element |
