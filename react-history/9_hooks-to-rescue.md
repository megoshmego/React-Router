Certainly! Here are the code snippets mentioned in the feedback:

1. Using Hooks:
```jsx
import React, { useState } from 'react';

const Counter = () => {
  const [count, setCount] = useState(0);

  const increment = () => {
    setCount(prevCount => prevCount + 1);
  };

  const decrement = () => {
    setCount(prevCount => prevCount - 1);
  };

  return (
    <div>
      <h3>Count is {count}</h3>
      <button onClick={increment}>Increment</button>
      <button onClick={decrement}>Decrement</button>
    </div>
  );
};
```

2. Creating a Custom Hook:
```jsx
import { useState } from 'react';

const useCounter = () => {
  const [count, setCount] = useState(0);

  const increment = () => {
    setCount(prevCount => prevCount + 1);
  };

  const decrement = () => {
    setCount(prevCount => prevCount - 1);
  };

  return { count, increment, decrement };
};

const Counter = () => {
  const { count, increment, decrement } = useCounter();

  return (
    <div>
      <h3>Count is {count}</h3>
      <button onClick={increment}>Increment</button>
      <button onClick={decrement}>Decrement</button>
    </div>
  );
};
```

These code snippets demonstrate how to use hooks, specifically the `useState` hook, to manage state in functional components. The `useState` hook provides a way to declare state variables and functions to update them. In the second example, a custom hook called `useCounter` is created to encapsulate the state management logic, allowing it to be reused in different components.