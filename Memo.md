# ⚙️ Avoid Re-Rendering with `React.memo` 🚀

`React.memo` is a higher-order component (HOC) in React that optimizes the performance of functional components by memoizing their output. It prevents re-renders if the props passed to the component haven't changed.

## When to Use `React.memo`

- Use it for **functional components** that receive props.
- It is useful when the component re-renders unnecessarily with the same props.
- Avoid using it if the component already updates infrequently, as it adds overhead.

## Syntax

```jsx
import React from 'react';

const MyComponent = (props) => {
  console.log('Rendering MyComponent');
  return <div>{props.value}</div>;
};

export default React.memo(MyComponent)
```

Here, MyComponent will only re-render if props.value changes.

### Done ! ⭐
