## ⚙️ Optimize React Component Re-Renders with useCallback 🚀

#### When passing functions as props to child components, wrap them with useCallback to prevent unnecessary re-renders.

Without `useCallback`:

```jsx
const Parent = () => {
  const handleClick = () => console.log('Clicked!');

  return <Child onClick={handleClick} />;
};
```

This causes `Child` to re-render every time Parent renders because `handleClick` is recreated.

With `useCallback`:

```jsx
import { useCallback } from 'react';

const Parent = () => {
  const handleClick = useCallback(() => console.log('Clicked!'), []);

  return <Child onClick={handleClick} />;
};
```

Now, `handleClick` is memoized, and `Child` won't re-render unnecessarily. This improves performance in large applications!

### Done ! ⭐
