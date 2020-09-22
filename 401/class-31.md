# Hooks

## Examples

### Function Component Hooks
```js
import React, { useState } from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"  const [count, setCount] = useState(0);
  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

### Class's CanNOT use Hooks
```js
class Example extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0
    };
  }

  render() {
    return (
      <div>
        <p>You clicked {this.state.count} times</p>
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>
          Click me
        </button>
      </div>
    );
  }
}
```

## The Hook
```js
import React, { useState } from 'react';
function Example() {
  // ...
}
```
A hook is a special function that lets you hook into React features. Example, `useState` is a hook that lets you add React state function components

##### Resources
https://reactjs.org/docs/hooks-state.html
