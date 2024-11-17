# ⚙️ Ensure Type safety with Prop Types 🚀

To ensure type safety with PropTypes in React, you define the expected types for props passed to a component. Here's how you can use PropTypes:

### Install PropTypes (if not already installed):

```bash
npm install prop-types
```

### Define PropTypes: 

In your component, you can specify the expected prop types like this:

```jsx
import PropTypes from 'prop-types';

const MyComponent = ({ name, age }) => {
  return (
    <div>
      <p>Name: {name}</p>
      <p>Age: {age}</p>
    </div>
  );
};

MyComponent.propTypes = {
  name: PropTypes.string.isRequired,
  age: PropTypes.number.isRequired,
};

export default MyComponent;
```

### What PropTypes Offers:
- `PropTypes.string`: Ensures the prop is a string.
- `PropTypes.number`: Ensures the prop is a number.
- `PropTypes.bool`: Ensures the prop is a boolean.
- `PropTypes.array`: Ensures the prop is an array.
- `PropTypes.object`: Ensures the prop is an object.
- `.isRequired`: Makes the prop required.

Using PropTypes helps catch potential issues when props are passed incorrectly, making your React components safer and easier to debug.

### Done ! ⭐
