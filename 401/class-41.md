# React: Native

### Setup
Run `npx react-native init MyTestApp` to get started.

### Hello World Starter Code
```js
import React from 'react';
import { Text, View } from 'react-native';

const HelloWorldApp = () => {
  return (
    <View
      style={{
        flex: 1,
        justifyContent: "center",
        alignItems: "center"
      }}>
      <Text>Hello, world!</Text>
    </View>
  )
}
export default HelloWorldApp;
```

Notice that the code is very similar to normal React but the function willr eturn a `View` component with a child `Text` component.




### React vs. react-Native State
![](https://user-images.githubusercontent.com/20761166/61405629-48270680-a8a8-11e9-906e-aa80d51e51e3.png)
