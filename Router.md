# ⚙️ Create a simple router in React.js 🚀
### Quick Info:
- #### Step 1: Install react-router-dom
- #### Step 2: Set Up Routing in App.js
- #### Step 3: Run the Application

### Step 1: Install react-router-dom

First, make sure you have react-router-dom installed:

```bash
npm install react-router-dom
```

### Step 2: Set Up Routing in App.js:

Now, import the necessary components from react-router-dom in your App.js file and define your routes.

```jsx
// App.js
import React from 'react';
import { BrowserRouter as Router, Routes, Route, Link } from 'react-router-dom';
import Home from './Home';
import About from './About';
import Contact from './Contact';

const App = () => {
  return (
    <Router>
      <nav>
        <Link to="/">Home</Link> | <Link to="/about">About</Link> | <Link to="/contact">Contact</Link>
      </nav>

      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </Router>
  );
};

export default App;
```
Router: Wraps your app to enable routing. <br />
Routes and Route: Define the route paths and specify the components to render for each path. <br />

### Step 3: Run the Application:

Finally, you can start your React application to see your simple router in action:

```bash
npm start
```

### Done ! ⭐
