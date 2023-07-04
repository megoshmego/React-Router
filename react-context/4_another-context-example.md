

Certainly! Here are some code snippets to illustrate the concepts mentioned in the video:

1. Creating the theme context:
```javascript
// themecontext.js
import React from 'react';

const ThemeContext = React.createContext();

export default ThemeContext;
```

2. Using the theme context provider:
```javascript
// App.js
import React from 'react';
import ThemeContext from './themecontext';

const App = () => {
  return (
    <ThemeContext.Provider value="magenta">
      {/* Your app components */}
    </ThemeContext.Provider>
  );
};

export default App;
```

3. Consuming the theme context using `useContext`:
```javascript
// ChildComponent.js
import React, { useContext } from 'react';
import ThemeContext from '../themecontext';

const ChildComponent = () => {
  const color = useContext(ThemeContext);

  return (
    <button style={{ color }}>Button</button>
  );
};

export default ChildComponent;
```

4. Creating a separate `ThemeProvider` component:
```javascript
// ThemeProvider.js
import React, { useState } from 'react';
import ThemeContext from './themecontext';

const ThemeProvider = ({ children }) => {
  const [color, setColor] = useState('orange');

  const toggleTheme = () => {
    setColor((prevColor) => (prevColor === 'olive' ? 'orange' : 'olive'));
  };

  return (
    <ThemeContext.Provider value={{ color, toggleTheme }}>
      {children}
    </ThemeContext.Provider>
  );
};

export default ThemeProvider;
```

5. Using the `ThemeProvider` in the App component:
```javascript
// App.js
import React from 'react';
import ThemeProvider from './ThemeProvider';
import ChildComponent from './ChildComponent';
import Navbar from './Navbar';

const App = () => {
  return (
    <ThemeProvider>
      <Navbar />
      <ChildComponent />
    </ThemeProvider>
  );
};

export default App;
```

These code snippets demonstrate the concepts discussed in the video, including creating the theme context, using the context provider, consuming the context using `useContext`, and creating a separate `ThemeProvider` component to manage the theme state and provide it to the children components.