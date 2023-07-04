Certainly! Here are some code snippets to illustrate the concepts mentioned in the video:

1. Adding multiple values to the context using an object:
```javascript
// CountContext.js
import React from 'react';

const CountContext = React.createContext();

export default CountContext;
```

2. Providing multiple values in the context:
```javascript
// App.js
import React from 'react';
import CountContext from './CountContext';

const App = () => {
  const increment = () => {
    setCount((prevCount) => prevCount + 1);
  };

  return (
    <CountContext.Provider value={{ count, increment }}>
      {/* Your app components */}
    </CountContext.Provider>
  );
};

export default App;
```

3. Consuming the context and destructuring the values:
```javascript
// GreatGrandchild.js
import React, { useContext } from 'react';
import CountContext from './CountContext';

const GreatGrandchild = () => {
  const { count, increment } = useContext(CountContext);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={increment}>Increment</button>
    </div>
  );
};

export default GreatGrandchild;
```
