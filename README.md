# react-lineto

Draw a line between two elements in React.

[![Build Status](https://travis-ci.org/kdeloach/react-lineto.svg?branch=master)](https://travis-ci.org/kdeloach/react-lineto)

## Getting Started

```
yarn install
yarn run demo
```

Browse to [localhost:4567](http://localhost:4567).

## Components

### LineTo

Draw line between two DOM elements.

#### Example

```
import LineTo from 'react-lineto';

function render() {
    return (
        <div>
            <div className="A">Element A</div>
            <div className="B">Element B</div>
            <LineTo from="A" to="B" />
        </div>
    );
}
```

#### Properties

| Name        | Type   | Description                                    | Example Values
| ----------- | ------ | ---------------------------------------------- | --------------
| from\*      | string | CSS class name of the first element            |
| to\*        | string | CSS class name of the second element           |
| fromAnchor  | string | Anchor for starting point (Format: "x y")      | `top right`, `bottom center`, `left`, `100% 0`
| toAnchor    | string | Anchor for ending point (Format: "x y")        | `top right`, `bottom center`, `left`, `100% 0`
| delay       | number or bool | Force render after delay (ms)          | `0`, `1`, `100`, `true`
| className   | string | Desired CSS className for the rendered element |
| borderColor | string | Border color                                   | `#f00`, `red`, etc.
| borderStyle | string | Border style                                   | `solid`, `dashed`, etc.
| borderWidth | number | Border width (px)                              |
| zIndex      | number | Z-index offset                                 |
| within      | string | CSS class name of the desired container        |

\* Required

### Line

Draw line using pixel coordinates (relative to viewport).

#### Example

```
import { Line } from 'react-lineto';

function render() {
    return (
        <Line x0={0} y0={0} x1={10} y1={10} />
    );
}
```

#### Properties

| Name        | Type   | Description                                    | Example Values
| ----------- | ------ | ---------------------------------------------- | --------------
| x0\*        | number | First X coordinate                             |
| y0\*        | number | First Y coordinate                             |
| x1\*        | number | Second X coordinate                            |
| y1\*        | number | Second Y coordinate                            |
| className   | string | Desired CSS className for the rendered element |
| borderColor | string | Border color                                   | `#f00`, `red`, etc.
| borderStyle | string | Border style                                   | `solid`, `dashed`, etc.
| borderWidth | number | Border width (px)                              |
| zIndex      | number | Z-index offset                                 |
| within     | string | CSS class name of the desired container        |

\* Required
