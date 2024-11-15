# ⚙️ Using state variables in React.js with the useState hook 🚀

#### In React.js, the useState hook is used to manage state in functional components. It allows you to declare a state variable and a function to update it, enabling you to manage dynamic data in your components.

```jsx
import React, { useState } from "react";

function Example() {
  // Declare a state variable called "count" and a function to update it
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Current count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}

export default Example;
```

### Key Concepts
#### 1. Initial State:
  The argument passed to useState (e.g., 0 in useState(0)) is the initial value of the state variable.
#### 2. Destructuring:
  useState returns an array with two elements:
  - The current state value.
  - A function to update the state.
#### 3. Updating State:
  - Use the updater function (setCount in this case) to update the state value.
  - React ensures the component re-renders with the updated state.

### Best Practices

#### Avoid Direct State Mutation:
- Do not modify the state directly (e.g., `count++` or `user.name = "John"`). Use the updater function instead.

#### Keep State Minimal:
- Only store what’s necessary in the state to reduce complexity.

#### Using Functional Updates:
- When the new state depends on the previous state, use a callback function:
  
```jsx
  setCount((prevCount) => prevCount + 1);
```

### Done ! ⭐
