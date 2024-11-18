# ⚙️ Manage Global State with React.js Context API 🚀

The Context API in React is used to share data across multiple components without having to pass props down manually through every level of the component tree. It helps manage "global state" that multiple parts of your application need to access, such as:

- Themes (light/dark mode)
- User authentication details (like username, token, or role)
- App settings or preferences
- Language or localization settings

### 1. Create the Context
```jsx
import React, { createContext, useState, useContext } from 'react';

// Create a context
const ThemeContext = createContext();
```

### 2. Create a Provider Component

The provider will manage the state and provide the context value to its children.

```jsx
const ThemeProvider = ({ children }) => {
    const [theme, setTheme] = useState('light');

    const toggleTheme = () => {
        setTheme((prevTheme) => (prevTheme === 'light' ? 'dark' : 'light'));
    };

    return (
        <ThemeContext.Provider value={{ theme, toggleTheme }}>
            {children}
        </ThemeContext.Provider>
    );
};
```
### 3. Use the Context in a Child Component

Access the context value with `useContext`.

```jsx
const ThemeSwitcher = () => {
    const { theme, toggleTheme } = useContext(ThemeContext);

    return (
        <div
            style={{
                background: theme === 'light' ? '#fff' : '#333',
                color: theme === 'light' ? '#000' : '#fff',
                padding: '20px',
                textAlign: 'center',
            }}
        >
            <p>Current Theme: {theme}</p>
            <button onClick={toggleTheme}>Toggle Theme</button>
        </div>
    );
};
```

### 4. Wrap the App with the Provider

Ensure the provider wraps the components that need access to the context.

```jsx
const App = () => {
    return (
        <ThemeProvider>
            <ThemeSwitcher />
        </ThemeProvider>
    );
};

export default App;
```

### Done ! ⭐
